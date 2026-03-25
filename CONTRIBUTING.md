# Contributing to KiloCode Boilerplate

Thank you for your interest in contributing to the KiloCode Boilerplate! This project serves as a template for setting up KiloCode configurations in new projects.

## Getting Started

1. Fork the repository
2. Create a new branch for your feature or bug fix
3. Make your changes
4. Submit a pull request

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

## Contribution Guidelines

- Keep changes focused and atomic
- Update documentation when making changes to functionality
- Follow the existing code style and conventions
- Test your changes before submitting

## Types of Contributions

We welcome contributions in the form of:
- Bug reports and fixes
- Feature enhancements
- Documentation improvements
- New skill templates
- Updated workflows

## Pull Request Process

1. Ensure your PR addresses a single issue or adds a single feature
2. Update the README.md with details of changes if applicable
3. Add or update tests if applicable
4. Make sure all checks pass before requesting review

## Questions?

If you have questions about contributing, feel free to open an issue for discussion.

Thank you for helping improve the KiloCode Boilerplate!