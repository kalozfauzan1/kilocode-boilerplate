# KiloCode Boilerplate

A framework-agnostic boilerplate for setting up KiloCode configurations in new projects.

## Overview

This boilerplate provides a standardized setup for KiloCode with:

- Universal configurations that work across different frameworks and languages
- Template files with placeholders for project-specific customization
- Recommended skills organized by category
- Serena workflow integration
- Manual configuration instructions to analyze codebases and create/update AGENTS.md files
- Codebase indexing capabilities when KiloCode's native indexing is enabled

## Quick Start

1. Clone this repository as a template for your new project
2. Customize the configuration files with your project details
3. Add framework-specific skills as needed
4. Manually configure your AGENTS.md file with your project-specific information
5. Start using KiloCode with consistent patterns

## Using This Boilerplate in Existing Projects

If you have an existing project and want to integrate KiloCode with this boilerplate:

### Option 1: Copy Files Directly
1. Copy the `.kilocode/` directory to your project root
2. Copy `AGENTS.md`, `mcp.json`, `README.md`, and `init-command.md` to your project root
3. Update `AGENTS.md` with your project's specific stack, commands, and conventions
4. Review and customize the mode-specific rules in `.kilocode/rules-*` directories as needed
5. Manually update AGENTS.md with your project-specific information

### Option 2: Git Submodule Approach
1. Add this repository as a submodule:
   ```bash
   git submodule add https://github.com/your-username/kilocode-boilerplate.git .kilocode-template
   ```
2. Copy the necessary files from the submodule to your project
3. Configure your project-specific settings

### Option 3: Fork and Customize
1. Fork this repository
2. Customize the templates for your organization's specific needs
3. Use your forked version as the template for all your projects

## Customization Guide

After copying the boilerplate files to your project:

1. **Update `AGENTS.md`** with your project's:
   - Technology stack
   - Build/deploy commands
   - Project-specific conventions
   - Framework-specific patterns

2. **Configure `.kilocode/config.json`** with your:
   - API keys and endpoints
   - Preferred models
   - Temperature and token settings

3. **Customize mode-specific rules** in `.kilocode/rules-*` directories based on your project's requirements

4. **Add framework-specific skills** in the appropriate skills directories if needed

5. **Manually update AGENTS.md** with your project-specific information

## Manual Configuration Process

The boilerplate includes instructions for manually configuring your AGENTS.md file with project-specific, non-obvious information:

1. Analyze your codebase to discover:

   - Build/lint/test commands
   - Code style guidelines
   - Project-specific patterns and conventions
   - Non-obvious gotchas and requirements

2. Update AGENTS.md files with only essential information that would surprise an experienced developer

3. Remove all standard practices and framework defaults to keep the files concise and valuable

See [init-command.md](init-command.md) for the complete configuration process definition.

## Configuration Files

### Core Configuration

- [`.kilocode/config.json`](.kilocode/config.json) - API and model configurations
- [`.kilocode/mcp.json`](.kilocode/mcp.json) - MCP server configurations
- [`mcp.json`](mcp.json) - Root-level MCP configuration

### Mode-Specific Rules

- [`.kilocode/rules-ask/AGENTS.md`](.kilocode/rules-ask/AGENTS.md) - Ask mode rules
- [`.kilocode/rules-code/AGENTS.md`](.kilocode/rules-code/AGENTS.md) - Code mode rules
- [`.kilocode/rules-architect/AGENTS.md`](.kilocode/rules-architect/AGENTS.md) - Architect mode rules
- [`.kilocode/rules-debug/AGENTS.md`](.kilocode/rules-debug/AGENTS.md) - Debug mode rules
- [`.kilocode/rules-orchestrator/AGENTS.md`](.kilocode/rules-orchestrator/AGENTS.md) - Orchestrator mode rules

### Workflows

- [`.kilocode/workflows/serena-setup.md`](.kilocode/workflows/serena-setup.md) - Setup workflow
- [`.kilocode/workflows/serena-dev-workflow.md`](.kilocode/workflows/serena-dev-workflow.md) - Development workflow
- [`.kilocode/workflows/serena-general.md`](.kilocode/workflows/serena-general.md) - General workflow

### Skills

The boilerplate includes universal skills organized by category:

- **Ask Skills** - Clarification and documentation skills
- **Architect Skills** - Architecture and design skills
- **Orchestrator Skills** - Task management and coordination
- **Review Skills** - Quality and security analysis
- **Docs Specialist Skills** - Documentation generation

## Customization

1. Update [AGENTS.md](AGENTS.md) with your project's stack and commands (following the manual configuration process)
2. Customize mode-specific rules in `.kilocode/rules-*` directories
3. Add framework-specific skills as needed (see below)
4. Update environment-specific configurations

## Codebase Indexing

This boilerplate works seamlessly with KiloCode's native Codebase Indexing feature. When enabled, the AI will automatically use semantic search to find relevant code across your project.

### Enabling Codebase Indexing

1. Open KiloCode settings in VS Code
2. Navigate to "Codebase Indexing" section
3. Enable the toggle switch
4. Configure your embedding provider (OpenAI, Gemini, or Ollama)
5. Set up Qdrant URL (e.g., `http://localhost:6333`)
6. Save and start initial indexing

Once enabled, the AI will automatically use `codebase_search` for natural language queries about your codebase.

## Adding Framework-Specific Skills

1. Update [AGENTS.md](AGENTS.md) with your project's stack and commands (following the manual configuration process)
2. Customize mode-specific rules in `.kilocode/rules-*` directories
3. Add framework-specific skills as needed (see below)
4. Update environment-specific configurations

## Adding Framework-Specific Skills

Use the prompt in [ADD-SKILLS-PROMPT.md](ADD-SKILLS-PROMPT.md) to get AI recommendations for skills specific to your project's framework and requirements.

## Project Structure

```
kilocode-boilerplate/
├── .kilocode/
│   ├── config.json                    # Universal - API/model configs
│   ├── mcp.json                       # Universal - MCP servers
│   ├── rules-ask/                     # Template - Ask mode rules
│   ├── rules-code/                    # Template - Code mode rules
│   ├── rules-architect/               # Template - Architect mode rules
│   ├── rules-debug/                   # Template - Debug mode rules
│   ├── rules-orchestrator/            # Template - Orchestrator mode rules
│   ├── workflows/                     # Universal - Workflow definitions
│   └── skills-*/                      # Universal and template skills
├── AGENTS.md                          # Template - Main documentation
├── mcp.json                           # Universal - Root MCP config
├── README.md                          # This file
├── ADD-SKILLS-PROMPT.md               # Prompt for skill recommendations
└── init-command.md                    # Automated initialization command
```

## License

MIT

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to get started.
