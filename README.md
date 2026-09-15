# Cursor personal skills

Personal [Cursor](https://cursor.com) agent skills, kept in git and installed into `~/.cursor/skills/` so they are available across all projects.

Cursor loads each personal skill from `~/.cursor/skills/<name>/SKILL.md`. The `skills/` directory in this repository uses the same layout. Do not sync `~/.cursor/skills-cursor/`: that tree is reserved for Cursor's built-in skills.

## Sync

Run these from the repository root. Trailing slashes copy directory _contents_ (not the `skills` folder itself).

Install or update skills from this repo into Cursor:

```bash
rsync -av skills/ ~/.cursor/skills/
```

Copy existing local skills from Cursor into this repo:

```bash
rsync -av ~/.cursor/skills/ skills/
```

## Skills

- [`commit-message`](skills/commit-message/SKILL.md) — propose a git commit title and body (`/commit-message`)
