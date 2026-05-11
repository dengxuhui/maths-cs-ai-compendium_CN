# AGENTS.md

> 面向未来 AI 会话的快速参考。每条均为不读此文件可能出错的高价值信息。

## 项目性质

这是上游英文教科书（HenryNdubuaku/maths-cs-ai-compendium）的**中文 fork**，核心工作是翻译与维护内容，而非开发软件功能。

## 常用命令

```bash
# 本地预览文档（访问 http://127.0.0.1:8000）
pip install "mkdocs<2" "mkdocs-material[imaging]"
mkdocs serve

# 手动部署（CI 在 push main 时自动触发）
mkdocs gh-deploy --force

# MCP 服务器（在 mcp/ 目录下，自动安装依赖再启动）
cd mcp && npm start
```

> **注意**：CI（`.github/workflows/deploy-docs.yml`）在构建时动态创建 `docs/` 目录并用符号链接指向章节目录。本地 `mkdocs serve` 需要先手动执行相同的 `mkdir -p docs` + 符号链接步骤，或直接在根目录运行（mkdocs 会读取 `docs_dir: docs`）。若本地预览报找不到文件，参考 CI 脚本手动建立 `docs/` 符号链接。

## 目录与文件命名规则

- 章节目录：`chapter XX: name/`（空格和冒号都是目录名的一部分）
- Section 文件：`XX. section name.md`
- 特例：第 14 章入口为 `00. foundations.md`，第 16 章入口为 `00. why C++ and how ML frameworks work.md`

## 新增或修改内容时必须同步

1. `mkdocs.yml` 的 `nav` 导航树（否则页面不出现在站点中）
2. `llms.txt`（MCP `recommend` 工具依赖此文件做关键词匹配）

## 数学公式

- 行内：`$...$`，独立块：`$$...$$`
- MkDocs 构建时由 MathJax 渲染，编辑时无需特殊处理

## MCP 服务器（`mcp/`）

- 入口：`mcp/src/index.ts`，使用 `tsx` 直接运行（无需编译步骤）
- 5 个工具：`list_topics`、`read_section`、`search`、`recommend`、`get_examples`
- `recommend` 解析 `llms.txt`，新增章节后务必更新该文件

## 章节状态

- 第 1–18 章：已完成（Available）
- 第 19–20 章：进行中（Coming），暂无 Markdown 文件

## 不需要关注的事项

- 没有测试套件、lint 或 typecheck 流程（MCP 服务器除外，但也无测试）
- 没有数据库、环境变量或密钥配置
