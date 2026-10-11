# Laws of UX — Agent Skill

A compact, drop-in skill that teaches AI coding/design agents the 10 core UX psychology principles (Jakob's, Fitts's, Hick's, Miller's, Postel's, Peak–End, Aesthetic-Usability, Von Restorff, Tesler's, Doherty Threshold) so they can apply them when designing or reviewing interfaces.

The skill follows the open `SKILL.md` format (YAML frontmatter + Markdown body), so it works with any agent that supports skills, and the body is plain Markdown you can paste into any AI tool's custom instructions.

**⬇️ [Download the latest release](https://github.com/sebastiansiju/laws-of-ux-skill/releases/latest)** · **👀 [See an example review](examples/signup-form-review.md)**

## What's inside

```
laws-of-ux-skill/
├── ux-laws-review/
│   └── SKILL.md                  # the skill itself
├── examples/
│   └── signup-form-review.md     # sample output
├── README.md
└── LICENSE
```

## Install

### Claude (claude.ai / desktop)
1. Zip the `ux-laws-review` folder (the folder, not just the file).
2. Go to **Settings → Capabilities → Skills** and upload the zip.

### Claude Code
```bash
# personal (all projects)
mkdir -p ~/.claude/skills && cp -r ux-laws-review ~/.claude/skills/

# or per project
mkdir -p .claude/skills && cp -r ux-laws-review .claude/skills/
```

### Other agents / tools (Cursor, Copilot, ChatGPT, etc.)
Copy the body of `ux-laws-review/SKILL.md` (everything below the `---` frontmatter) into the tool's rules file or custom instructions — e.g. `.cursor/rules/ux-laws-review.md` or `.github/copilot-instructions.md`.

## Usage

Ask your agent things like:
- "Review this signup form against the Laws of UX."
- "Which UX law explains why our checkout feels slow?"
- "Redesign this settings page — keep Hick's and Miller's Law in mind."

The agent will flag issues by law name, which gives you shared vocabulary with designers and clients.

## Credits

The principles are summarised from Jon Yablonski's *Laws of UX* (O'Reilly, 2020) and the free companion site **[lawsofux.com](https://lawsofux.com)**. This repo contains original short summaries only — no text is reproduced from the book. If you find this useful, go read the book and the site; they go much deeper.

The underlying laws themselves come from decades of HCI and psychology research (Fitts 1954, Hick 1952, Miller 1956, Postel's RFC 761, Kahneman's peak–end research, and others).

## Contributing

PRs welcome — e.g. adding examples per law, a short "bad vs good" pattern for each, or translations. Please keep summaries in your own words and credit sources.

## License

MIT — see [LICENSE](LICENSE). Applies to the text in this repo, not to the *Laws of UX* book or website.
