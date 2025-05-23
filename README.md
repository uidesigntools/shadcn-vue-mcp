# ShadcnVue MCP Server - A powerful AI Agent tool that helps developers instantly create high-quality UI components

[![smithery badge](https://smithery.ai/badge/@HelloGGX/shadcn-vue-mcp)](https://smithery.ai/server/@HelloGGX/shadcn-vue-mcp)

[![中文文档](https://img.shields.io/badge/docs-中文版-yellow)](./docs/README.zh-CN.md)

Shadcn-vue MCP Server is a powerful AI-driven tool that helps developers instantly create beautiful, modern UI components through natural language descriptions. It integrates the shadcn-vue component library and tailwindcss, seamlessly connects with mainstream IDEs, and provides a streamlined UI development workflow.

## ❌ Without shadcn-vue MCP

Developers face multiple challenges when building UI components:

- ❌ Need to manually check shadcn-vue and tailwindcss4.0 documentation, wasting significant time
- ❌ Component code needs to be written from scratch, inefficient
- ❌ Difficult to achieve design consistency, components lack unified style
- ❌ Hard to implement high-quality components that meet design and coding standards

## ✅ With shadcn-vue MCP

shadcn-vue MCP provides an intelligent UI component development experience:

- 1️⃣ Simply describe your desired component in natural language
- 2️⃣ MCP automatically generates code compliant with shadcn-vue and tailwindcss standards
- 3️⃣ Get production-ready, design-consistent shadcn-vue UI components

Example usage:

```txt
/ui create a navigation bar component 
```

```txt
/refine optimize the navbar's responsiveness and accessibility
```

 advantages:
- Real-time access to latest shadcn-vue component specifications
- Generated code 100% compliant with current version requirements
- Based on the LLM.txt file provided by context7 as context, more accurate code generation is achieved
- No more repeatedly checking documentation or worrying about version compatibility
- Seamless multi-IDE workflow integration

### Features

- AI-powered UI generation: Create UI components through natural language descriptions
  **Multi-IDE Support**:
  - [Cursor](https://cursor.com) IDE integration
  - [Trae](https://www.trae.ai/) support
  - [VSCode](https://code.visualstudio.com/) support
  - [VSCode + Cline](https://cline.bot) integration (Beta)
- Modern component library: Based on shadcn-vue component library and tailwindcss
- TypeScript support: Full TypeScript support for type-safe development
- Intelligent shadcn-vue component documentation query
- Component enhancement: Accessibility support/performance optimization/advanced design improvements/animation improvements
- Real-time component preview generation (coming soon).

## Prerequisite

Node.js version 22 or above.

## Getting Started

### Installing via Smithery

1. **Go to **https://openrouter.ai/models** to register an account, obtain OPENROUTER_API_KEY, and view available model lists**

2. **Choose installation method**

#### Method 1: CLI Quick Installation

To install bazi-mcp for Claude Desktop automatically via [Smithery](https://smithery.ai/server/@HelloGGX/shadcn-vue-mcp):

```bash
npx -y @smithery/cli@latest install @HelloGGX/shadcn-vue-mcp --client vscode
```

Supported clients: cursor, windsurf, cline, claude, vscode, vscode-insiders

#### Method 2: Manual Configuration

Manually configure AI application (e.g. Claude Desktop).

```json
{
  "mcpServers": {
    "shadcn-vue": {
      "command": "npx",
      "args": ["-y", "@agent/shadcn-vue"],
      "env": {
        "OPENROUTER_MODEL_ID": "Your selected OpenRouter model id",
        "OPENROUTER_API_KEY": "Your OpenRouter API key"
      }
    }
  }
}
```

Config file locations:

- Cursor: `~/.cursor/mcp.json`
- Trae: `~/.Trae/mcp.json`
- Cline: `~/.cline/mcp_config.json`
- Claude: `~/.claude/mcp_config.json`

## Tools List

### read-usage-doc

> Query component documentation

#### Arguments

- name: `String`
  > shadcn-vue component name. Example: "button component usage documentation"

### read-full-doc

> Read full documentation of a component  
> Use this tool when mentions /doc.

#### Arguments

- name: `String`
  > shadcn-vue component name. Example: "button component full documentation"

### create-ui

> Create UI components  
> Create Web UI with shadcn/ui components and tailwindcss, Use this tool when mentions /ui

#### Arguments

- description: `String`
  > Description of component requirements. Example: "/ui create a flight display component"

### refine-code

> Enhance and optimize specified component code
> Refine code, Use this tool when mentions /refine

#### Arguments

- userMessage: `String`
  > Code to be optimized. Example: "/refine optimize this code to have mobile responsive layout"
- absolutePathToRefiningFile: `String`
  > Absolute path to the file that needs refinement.
- context: `String`
  > Extract specific UI elements and aspects needing improvement based on user messages, code, and conversation history.

## Result Example

User: /ui create a flight display component

AI: Generated code as follows:

![UI Component Example](https://github.com/HelloGGX/tailwindcss-mcp/raw/main/docs/ui.png)

## 🤝 Contribution Guide

We welcome all contributions! Help us improve @agent/shadcn-vue. Source code is open-sourced on [GitHub](https://github.com/HelloGGX/shadcn-vue-mcp).

## 👥 Community & Support

- [Discord Community](https://discord.gg/82Kf65ut) - Join our active community

## 📝 License

MIT License

---
