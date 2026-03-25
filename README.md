# KiloCode Boilerplate

A framework-agnostic boilerplate for setting up KiloCode configurations in new projects, providing standardized patterns for AI-assisted development.

## Overview

This boilerplate simplifies KiloCode setup with:

- **Universal configurations** - Works across frameworks and languages
- **Template files** - Ready for project-specific customization
- **Organized skills** - Categorized by mode (Ask, Code, Architect, Debug, Orchestrator, Review)
- **Workflow integration** - Serena workflow for enhanced code intelligence
- **Automated initialization** - `init` command analyzes codebases and creates AGENTS.md files
- **Codebase indexing** - Semantic search for natural language queries (when enabled)

## Quick Start

### For New Projects
1. Clone this repository as a template
2. Run the `init` command to automatically analyze your codebase and generate AGENTS.md files
3. Customize configurations as needed

### For Existing Projects

#### Option 1: Copy Files Directly
1. Copy the `.kilocode/` directory to your project root
2. Copy `AGENTS.md`, `mcp.json`, and `init-command.md` to your project root
3. Run the `init` command to analyze your codebase
4. Review and customize mode-specific rules in `.kilocode/rules-*` directories

#### Option 2: Git Submodule Approach
1. Add this repository as a submodule:
   ```bash
   git submodule add https://github.com/kilocode/kilocode-boilerplate.git .kilocode-template
   ```
2. Copy necessary files from the submodule to your project
3. Run the `init` command to configure

#### Option 3: Fork and Customize
1. Fork this repository
2. Customize templates for your organization's needs
3. Use your forked version as the template for all projects

## Key Features

### Automated Initialization

The `init` command ([init-command.md](init-command.md)) is a powerful tool that:
- Analyzes your codebase to discover non-obvious, project-specific information
- Creates or updates AGENTS.md files with only essential information
- Focuses on details that would surprise an experienced developer
- Preserves existing designed rules and workflows
- Generates mode-specific files in `.kilocode/rules-*/` directories

### Configuration Files

| File | Purpose |
|------|---------|
| [`AGENTS.md`](AGENTS.md) | Main project documentation (template) |
| [`mcp.json`](mcp.json) | Root-level MCP server configuration |
| [`.kilocode/config.json`](.kilocode/config.json) | API and model configurations |
| [`.kilocode/mcp.json`](.kilocode/mcp.json) | MCP server configurations |
| [`.kilocode/rules-*/AGENTS.md`](.kilocode/rules-ask/AGENTS.md) | Mode-specific rules (Ask, Code, Architect, Debug, Orchestrator) |
| [`.kilocode/workflows/`](.kilocode/workflows/) | Serena workflow definitions |
| [`.kilocode/skills-*/`](.kilocode/skills-ask/) | Universal skills organized by category |

### Codebase Indexing

Enable KiloCode's Codebase Indexing for semantic search:
1. Open KiloCode settings in VS Code
2. Navigate to "Codebase Indexing" section
3. Enable the toggle switch
4. Configure your embedding provider (OpenAI, Gemini, or Ollama)
5. Set up Qdrant URL (e.g., `http://localhost:6333`)
6. Save and start initial indexing

Once enabled, the AI will automatically use `codebase_search` for natural language queries.

## Customization

After initial setup, customize the boilerplate:

1. **Update AGENTS.md** - Add your project's stack, commands, and conventions
2. **Configure .kilocode/config.json** - Set API keys, preferred models, and temperature/token settings
3. **Customize mode-specific rules** - Modify `.kilocode/rules-*` directories
4. **Add framework-specific skills** - Use [ADD-SKILLS-PROMPT.md](ADD-SKILLS-PROMPT.md) to get AI recommendations

## Project Structure

```
kilocode-boilerplate/
├── .kilocode/
│   ├── config.json                    # API/model configurations
│   ├── mcp.json                       # MCP server configurations
│   ├── rules-ask/                     # Ask mode rules
│   ├── rules-code/                    # Code mode rules
│   ├── rules-architect/               # Architect mode rules
│   ├── rules-debug/                   # Debug mode rules
│   ├── rules-orchestrator/            # Orchestrator mode rules
│   ├── workflows/                     # Serena workflow definitions
│   └── skills-*/                      # Universal and template skills
├── AGENTS.md                          # Main project documentation template
├── mcp.json                           # Root MCP configuration
├── README.md                          # This file
├── ADD-SKILLS-PROMPT.md               # Skill recommendation prompt
└── init-command.md                    # Automated initialization command
```

## License

MIT

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.