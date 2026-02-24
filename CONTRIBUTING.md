# Contributing to GeneBoyleSkills

## Who Can Contribute

- **Kelly Boyle** — Primary maintainer. Builds, updates, and manages all skills.
- **Gene Boyle** — Reviews content that represents his public voice (avatar, social media, client comms).
- **Claude** — Generates skill drafts and updates via conversation, pushed by Kelly or Gene.

## How Skills Work

Each skill is a folder containing a `SKILL.md` file with YAML frontmatter:

```yaml
---
name: skill-name
description: >
  When and how this skill should trigger. Be specific and "pushy" —
  Claude tends to under-trigger, so descriptions should cast a wide net.
---
```

Optional `references/` subdirectory for deep-dive reference docs that SKILL.md points to.

## Adding a New Skill

1. Create a new folder: `skill-name/`
2. Add `SKILL.md` with valid frontmatter (name + description required)
3. Add `references/` directory if needed
4. Test by asking Claude a question the skill should handle
5. Push to `main` (or create a PR if branch protection is enabled)

## Updating an Existing Skill

- Edit directly on GitHub (click the pencil icon on any `.md` file)
- Or clone locally, edit, and push
- Claude always fetches the latest version from `main`

## Rules

1. **No secrets** — Never commit tokens, API keys, passwords, or client data
2. **No client-identifiable information** — Anonymize all case studies and examples
3. **Gene's voice matters** — Any skill that generates content "as Gene" must match his voice principles in `avatar/SKILL.md`
4. **Always search first** — Skills that reference market data must instruct Claude to search before responding
5. **Keep it current** — If probate code, court procedures, or market conditions change, update the affected skills
