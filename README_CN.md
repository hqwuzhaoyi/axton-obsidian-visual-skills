# Obsidian 可视化 Skills 套装

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**[English](README.md)**

让 Claude Code 在 Obsidian 里生成 Canvas / Excalidraw / Mermaid 的可视化三件套。

## 什么是 Skills?

Skills 是 [Claude Code](https://docs.anthropic.com/en/docs/claude-code) 的提示词扩展，赋予 Claude 专业化能力。与需要配置的 MCP 服务器不同，Skills 只是简单的 Markdown 文件，Claude 会按需加载。

## 包含的 Skills

### 1. Excalidraw 图表生成器

使用 Obsidian 的 Excalidraw 插件直接生成手绘风格图表。

**特性：**
- 8 种图表类型：流程图、思维导图、层级图、关系图、对比图、时间线、矩阵图、自由布局
- 自动保存为 Obsidian 可用的 `.md` 文件
- 手绘美学风格，样式统一
- 完美支持中文

**触发词：** `Excalidraw`、`画图`、`流程图`、`思维导图`

### 2. Mermaid 可视化器

将文本内容转换为专业的 Mermaid 图表，适用于演示和文档。

**特性：**
- 多种图表类型：流程图、时序图、思维导图、状态图
- 内置语法错误预防机制
- 可配置布局、详细程度和配色方案
- 兼容 Obsidian、GitHub 等 Mermaid 渲染器

**触发词：** `Mermaid`、`可视化`、`流程图`、`时序图`

### 3. Obsidian Canvas 创建器

创建交互式 Obsidian Canvas 文件，支持思维导图和自由布局。

**特性：**
- 两种布局模式：思维导图（放射状层级）和自由布局（自定义位置）
- 根据内容长度智能调整节点大小
- 自动创建关系连线
- 支持预设颜色和自定义颜色

**触发词：** `Canvas`、`思维导图`、`可视化图表`

## 安装

### 前置要求

- 已安装 [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code)
- [Obsidian](https://obsidian.md/) 及相关插件：
  - [Excalidraw 插件](https://github.com/zsviczian/obsidian-excalidraw-plugin)（用于 Excalidraw skill）

### 安装 Skills

将 skill 文件夹复制到 Claude Code 的 skills 目录：

```bash
# 克隆仓库
git clone https://github.com/axtonliu/axton-obsidian-visual-skills.git

# 复制 skills 到 Claude Code 目录
cp -r axton-obsidian-visual-skills/excalidraw-diagram ~/.claude/skills/
cp -r axton-obsidian-visual-skills/mermaid-visualizer ~/.claude/skills/
cp -r axton-obsidian-visual-skills/obsidian-canvas-creator ~/.claude/skills/
```

也可以按需只复制单个 skill。

## 使用方法

安装后，当你请求可视化内容时，Claude Code 会自动使用这些 skills：

```
# Excalidraw
"创建一个展示 CI/CD 流程的 Excalidraw 流程图"
"画一个关于机器学习概念的思维导图"

# Mermaid
"用 Mermaid 图表可视化这个流程"
"为 API 调用创建时序图"

# Canvas
"把这篇文章转换成 Obsidian Canvas"
"创建一个项目规划的思维导图 Canvas"
```

## 文件结构

```
axton-obsidian-visual-skills/
├── excalidraw-diagram/
│   ├── SKILL.md           # 主 skill 定义
│   ├── assets/            # 示例输出
│   └── references/        # 技术参考
├── mermaid-visualizer/
│   ├── SKILL.md
│   └── references/
├── obsidian-canvas-creator/
│   ├── SKILL.md
│   ├── assets/
│   └── references/
├── README.md
├── README_CN.md
└── LICENSE
```

## 贡献

欢迎贡献！你可以：

- 报告 Bug 或问题
- 建议新的图表类型或功能
- 改进文档
- 提交 Pull Request

## 许可证

MIT 许可证 - 详见 [LICENSE](LICENSE)。

## 作者

**Axton Liu** - AI 教育者与创作者

- YouTube: [@AxtonLiu](https://youtube.com/@AxtonLiu)
- Twitter/X: [@axtonliu](https://twitter.com/axtonliu)
