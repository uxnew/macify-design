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

Clone the repository, then copy the skill folder into your Codex skills directory:

```bash
git clone https://github.com/uxnew/macify-design.git
cd macify-design
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

Common placement options:

| Tool or host | How to use |
| --- | --- |
| ChatGPT Projects / Gemini / generic assistants | Paste `adapters/generic-system-prompt.md` into project or system instructions. |
| Cursor / Windsurf / Cline / Roo / Continue | Copy `adapters/editor-agent-instructions.md` into the tool's project rules or custom instructions file. |
| Claude Projects / Claude Code | Paste `adapters/claude-instructions.md` into project instructions, or copy it into `CLAUDE.md` when that is your agent convention. |
| VS Code / GitHub Copilot | Copy `adapters/github-copilot-instructions.md` into `.github/copilot-instructions.md` or the workspace's Copilot instructions surface. |
| v0 / Lovable / Bolt / Replit Agent | Paste `adapters/app-builder-prompt.md` together with the product request. |

Use `examples/decision-cases.md` to check whether a request should trigger the skill before pasting an adapter into a long-lived project.

## Core Rule

Design tool/workspace web products as coherent workbenches: product workflow first, Mac-like skin second. Desktop uses a windowed workbench; mobile uses a responsive app shell. Always support light and dark appearance, real states, and usable interactions.

## License

MIT.
