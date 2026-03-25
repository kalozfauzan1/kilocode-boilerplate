# Skill Recommendation Prompt

Copy and paste the following prompt to your AI assistant to get skill recommendations for your project:

---

**PROMPT START**

I have just set up KiloCode with the boilerplate configuration. Help me select and add the appropriate skills for my project.

**Project Context:**

- Framework/Language: [e.g., Next.js + TypeScript, Django + Python, Rust + Actix]
- Project Type: [e.g., Web frontend, API backend, Full-stack, CLI tool, Mobile app]
- Key Libraries: [e.g., React Query, Zustand, TailwindCSS / or: FastAPI, SQLAlchemy / or: etc.]
- Main Tasks: [e.g., Building UI components, API development, Database modeling, Testing]

Based on this context, please:

1. Recommend which skills I should add from the available skill categories
2. Explain why each skill is relevant to my project
3. Provide the exact commands or steps to add each recommended skill

**Available Skill Categories in Boilerplate:**

- `skills-ask/` - Clarification and documentation skills (universal)
- `skills-architect/` - Architecture diagram and tradeoff documentation
- `skills-orchestrator/` - Task decomposition and progress tracking
- `skills-review/` - Code quality, security, and test coverage analysis
- `skills-docs-specialist/` - API documentation generation

**Framework-Specific Skills (not included, suggest if needed):**

- React/Next.js: Zustand store generator, React Query hook generator, Tailwind class organizer, Component prop types extractor
- Python: [suggest based on ecosystem]
- Rust: [suggest based on ecosystem]
- Other: [suggest based on project needs]

**PROMPT END**
