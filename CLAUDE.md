# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目简介

这是《数学、CS 与 AI 百科全书》的中文 fork，是一本直觉优先的开源教科书，从零开始涵盖数学、计算机科学和人工智能，共 20 个章节（目前 18 章完成，第 19-20 章进行中）。

## 常用命令

### 文档本地预览

```bash
pip install mkdocs "mkdocs-material[imaging]"
mkdocs serve
```

### 文档部署

```bash
mkdocs gh-deploy --force
```

也可以直接 push 到 `main` 分支，GitHub Actions 会自动触发部署（见 `.github/workflows/deploy-docs.yml`）。

### MCP 服务器

```bash
cd mcp
npm start   # 自动安装依赖并启动
npm setup   # 仅安装依赖
```

## 整体架构

项目由四层组成：

**内容层** → **文档层** → **部署层** + **工具层**

- **内容层**：105 个 Markdown 文件，使用 MathJax 渲染 LaTeX 数学公式
- **文档层**：MkDocs + Material 主题，`mkdocs.yml` 定义完整导航树和 MathJax 配置
- **部署层**：GitHub Actions 自动构建并发布到 GitHub Pages
- **工具层**：TypeScript MCP 服务器（`mcp/src/index.ts`），让 AI 助手能访问本书内容

### MCP 服务器提供的 5 个工具

| 工具 | 功能 |
|------|------|
| `list_topics` | 列出所有章节和 section，可按章节号筛选 |
| `read_section` | 读取指定章节的完整内容 |
| `search` | 全文搜索（返回匹配行 + 上下文，最多 20 条） |
| `recommend` | 基于学习目标推荐 section（解析 `llms.txt`） |
| `get_examples` | 提取代码示例，支持按语言和章节过滤 |

### llms.txt

`llms.txt` 是 LLM 友好的内容索引，记录每个 section 的路径和描述。MCP 的 `recommend` 工具解析此文件做关键词匹配。**新增 section 后需同步更新此文件。**

## 内容编写规范

### 目录和文件命名

- 章节目录：`chapter XX: name/`（如 `chapter 01: vectors/`）
- Section 文件：`XX. section name.md`（如 `01. vector spaces.md`）
- 章节 14 有特殊编号 `00. foundations.md`

### 新增内容时需同步更新

1. `mkdocs.yml` 的 `nav` 导航树
2. `llms.txt` 的章节描述索引

### 数学公式

使用标准 LaTeX 语法，行内公式 `$...$`，独立公式 `$$...$$`，MkDocs 构建时由 MathJax 渲染。
