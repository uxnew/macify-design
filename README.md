# Macify Design

Macify Design is an AI skill and portable instruction set for designing web tool products with Mac-like skin, material layering, single-window workbench structure, light/dark appearance, responsive mobile app shells, and real product states.

It is not a macOS clone kit. It does not use Apple assets or simulate the operating system.

## Use It For

- Web tools and productivity products
- Admin systems and internal tools
- Dashboards and analytics consoles
- Editors and creation tools
- AI tools and agent workbenches
- CMS, CRM, publishing, and tutorial management systems
- Developer tools, monitoring consoles, automation builders
- Single-file HTML prototypes for tool/workspace products

Do not use it by default for marketing pages, blogs, passive documentation readers, article/video libraries, ecommerce storefronts, portfolios, games, or products with a stronger requested design system.

## Repository Structure

```text
macify-design/
├── skills/
│   └── macify-design/          # Codex/OpenAI skill
├── adapters/                   # Portable instructions for other AI tools
├── examples/                   # Trigger calibration examples
├── README.md
├── README.zh-CN.md
├── LICENSE
└── VERSION
```

## Install For Codex

Copy the skill folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R skills/macify-design ~/.codex/skills/macify-design
```

Then invoke it explicitly with `$macify-design`, or let it trigger on suitable web tool/workspace product requests.

## Use With Other AI Tools

Use the files in `adapters/`:

- `generic-system-prompt.md`: ChatGPT Projects, Gemini, generic assistants
- `editor-agent-instructions.md`: Cursor, Windsurf, Cline, Roo, Continue, editor agents
- `claude-instructions.md`: Claude Projects and Claude Code
- `github-copilot-instructions.md`: VS Code / GitHub Copilot workspace instructions
- `app-builder-prompt.md`: v0, Lovable, Bolt, Replit Agent, and prompt-to-app tools

These adapters are instruction files, not automatic installers. The canonical rules live in `skills/macify-design/SKILL.md` and its references.

## Core Rule

Design tool/workspace web products as coherent workbenches: product workflow first, Mac-like skin second. Desktop uses a windowed workbench; mobile uses a responsive app shell. Always support light and dark appearance, real states, and usable interactions.

## License

MIT.
