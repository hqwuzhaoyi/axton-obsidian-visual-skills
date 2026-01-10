# Obsidian Visual Skills Pack

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**[中文文档](README_CN.md)**

Visual Skills Pack for Obsidian: generate Canvas, Excalidraw, and Mermaid diagrams from text with Claude Code.

## What Are Skills?

Skills are prompt-based extensions for [Claude Code](https://docs.anthropic.com/en/docs/claude-code) that give Claude specialized capabilities. Unlike MCP servers that require setup, skills are simple markdown files that Claude loads on demand.

## Included Skills

### 1. Excalidraw Diagram Generator

Generate hand-drawn style diagrams directly in Obsidian using the Excalidraw plugin.

**Features:**
- 8 diagram types: Flowchart, Mind Map, Hierarchy, Relationship, Comparison, Timeline, Matrix, Freeform
- Auto-save `.md` files ready for Obsidian
- Hand-drawn aesthetic with consistent styling
- Chinese text support with proper font handling

**Trigger words:** `Excalidraw`, `diagram`, `flowchart`, `mind map`

### 2. Mermaid Visualizer

Transform text content into professional Mermaid diagrams optimized for presentations and documentation.

**Features:**
- Multiple diagram types: Process flows, Sequence diagrams, Mind maps, State diagrams
- Built-in syntax error prevention
- Configurable layouts, detail levels, and color schemes
- Compatible with Obsidian, GitHub, and other Mermaid renderers

**Trigger words:** `Mermaid`, `visualize`, `flowchart`, `sequence diagram`

### 3. Obsidian Canvas Creator

Create interactive Obsidian Canvas files with MindMap or freeform layouts.

**Features:**
- Two layout modes: MindMap (radial hierarchy) and Freeform (custom positioning)
- Smart node sizing based on content length
- Automatic edge creation for relationships
- Color-coded nodes with preset or custom colors

**Trigger words:** `Canvas`, `mind map`, `visual diagram`

## Installation

### Prerequisites

- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) installed
- [Obsidian](https://obsidian.md/) with relevant plugins:
  - [Excalidraw plugin](https://github.com/zsviczian/obsidian-excalidraw-plugin) (for Excalidraw skill)

### Install Skills

Copy the skill folders to your Claude Code skills directory:

```bash
# Clone the repository
git clone https://github.com/axtonliu/axton-obsidian-visual-skills.git

# Copy skills to Claude Code directory
cp -r axton-obsidian-visual-skills/excalidraw-diagram ~/.claude/skills/
cp -r axton-obsidian-visual-skills/mermaid-visualizer ~/.claude/skills/
cp -r axton-obsidian-visual-skills/obsidian-canvas-creator ~/.claude/skills/
```

Or copy individual skills as needed.

## Usage

Once installed, Claude Code will automatically use these skills when you ask for visualizations:

```
# Excalidraw
"Create an Excalidraw flowchart showing the CI/CD pipeline"
"Draw a mind map about machine learning concepts"

# Mermaid
"Visualize this process as a Mermaid diagram"
"Create a sequence diagram for the API flow"

# Canvas
"Turn this article into an Obsidian Canvas"
"Create a mind map canvas for project planning"
```

## File Structure

```
axton-obsidian-visual-skills/
├── excalidraw-diagram/
│   ├── SKILL.md           # Main skill definition
│   ├── assets/            # Example outputs
│   └── references/        # Technical references
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

## Contributing

Contributions are welcome! Feel free to:

- Report bugs or issues
- Suggest new diagram types or features
- Improve documentation
- Submit pull requests

## License

MIT License - see [LICENSE](LICENSE) for details.

## Author

**Axton Liu** - AI educator and creator

- YouTube: [@AxtonLiu](https://youtube.com/@AxtonLiu)
- Twitter/X: [@axtonliu](https://twitter.com/axtonliu)
