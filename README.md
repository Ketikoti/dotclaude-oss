# dotclaude-oss

> **The open-source `.claude/` system for Claude Code that actually ships.**
> Plan better. Build faster. Keep context clean.

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Stars](https://img.shields.io/github/stars/Ketikoti/dotclaude-oss?style=social)](https://github.com/Ketikoti/dotclaude-oss/stargazers)
[![Forks](https://img.shields.io/github/forks/Ketikoti/dotclaude-oss?style=social)](https://github.com/Ketikoti/dotclaude-oss/network/members)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

---

## Why dotclaude-oss?

Most Claude Code setups are one giant `CLAUDE.md` file that grows into an unmaintainable mess.
**dotclaude-oss** is different: it gives you a modular, team-ready `.claude/` folder structure with rules, commands, agents, and skills — all separated by concern, all reusable across projects.

Built over years of real-world agentic workflow experience across multi-service systems, trading platforms, and AI SaaS products.

---

## What's inside?

```
.claude/
├── CLAUDE.md              # Root project context (short & clean)
├── settings.json          # Permissions, hooks, model defaults
├── rules/
│   ├── code-style.md      # Coding conventions
│   ├── testing.md         # Test strategy & coverage rules
│   ├── api-conventions.md # API design standards
│   └── security.md        # OWASP-aligned security rules
├── commands/
│   ├── review.md          # /review — deep code review
│   ├── fix-issue.md       # /fix-issue — targeted bug fix
│   ├── spec.md            # /spec — write specs before building
│   ├── ship.md            # /ship — plan > implement > test > commit
│   └── refactor.md        # /refactor — safe structural cleanup
├── agents/
│   ├── code-reviewer.md   # Specialized review agent
│   ├── security-auditor.md# Security-focused audit agent
│   └── architect.md       # System design & architecture agent
└── skills/
    ├── feature-build.md   # End-to-end feature workflow
    ├── pr-review.md       # Pull request review workflow
    └── deploy.md          # Deployment checklist workflow
```

---

## Quick Start

```bash
# Clone into your project
git clone https://github.com/Ketikoti/dotclaude-oss.git
cp -r dotclaude-oss/.claude ./

# Or use as a template
# Click "Use this template" above
```

Then open your project in Claude Code — it will automatically pick up the `.claude/` folder.

---

## Core Principles

| Principle | What it means |
|---|---|
| **Modular over monolithic** | Rules, commands, agents and skills are separate files, not one giant blob. |
| **Plan first, execute second** | Every workflow enforces exploration and planning before writing code. |
| **Team-ready by default** | Designed for shared use — personal overrides stay local and untracked. |
| **Measurable quality** | Every command includes a definition of done and success criteria. |
| **Security-conscious** | OWASP-aligned security rules baked in, not bolted on. |

---

## Commands

Run these inside Claude Code with `/command-name`:

| Command | What it does |
|---|---|
| `/spec` | Write a detailed spec before touching code |
| `/ship` | Full workflow: plan → implement → test → commit |
| `/review` | Deep code review with checklist |
| `/fix-issue` | Targeted, safe bug fix workflow |
| `/refactor` | Structural cleanup without breaking functionality |

---

## Agents

| Agent | Specialty |
|---|---|
| `code-reviewer` | Finds bugs, style issues, and missing tests |
| `security-auditor` | OWASP-based vulnerability scanning |
| `architect` | System design, ADRs, and scalability review |

---

## Roadmap

- [x] Modular rules structure
- [x] Reusable commands
- [x] Specialized agents
- [ ] CI/CD integration workflow
- [ ] Multi-tenant project support
- [ ] Trading & fintech-specific rules pack
- [ ] Vedic / Sanskrit naming convention skill
- [ ] GitHub Actions for automated `.claude/` linting

---

## Contributing

PRs are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting.

This project follows the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md).

---

## Support & Sponsorship

If this project saves you time, consider sponsoring the maintainer:

[![GitHub Sponsors](https://img.shields.io/badge/Sponsor-%E2%9D%A4-pink?logo=github)](https://github.com/sponsors/Ketikoti)

Your support funds continued development of open-source AI tooling, agentic systems, and developer productivity tools.

---

## License

Apache License 2.0 — see [LICENSE](LICENSE) for details.
Free for personal and commercial use.

---

<p align="center">
  <strong>Built for developers who ship.</strong><br>
  Star this repo if it helps you build better with Claude Code.
</p>
