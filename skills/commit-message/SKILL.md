---
name: commit-message
description: Propose a short git commit title and body from staged and working-tree changes. Use when the user invokes /commit-message.
disable-model-invocation: true
---

Propose a short commit title + body message for the changes (staged and in the working tree).

Identification/best-effort:

- Inspect the previous commit messages to find a pattern and reuse it if possible (style, length, etc.).
- Identify if the commit is stand-alone or part of a larger feature/bugfix commit chain.
- Look at the **branch name** and related **issue** to find clues about the **purpose** of the commit.
- Identify the **implementation details** using the **commit history**, the **codebase**, and **diff tools**.

Rules:

- The commit **title** should be a single line of text focusing on the **purpose** of the commit.
- The commit **title** start with an action verb (e.g. `Add`, `Fix`, `Refactor`, `Update`, `Remove`, `Move`, `Rename`, `Change`, `Improve`, `Optimize`, `Simplify`, `Refine`, ...).
- If the commit is a typo fix or similar minor change, leave the **body empty**.
- Otherwise, add one blank line between the **title** and the **body**.
- **Implementation details**, if necessary, are best kept in the **commit body**.
- If the commit is an obvious fix for a registered issue, add `Close #<issue-number>` or `Fix #<issue-number>` as a **trailer** after the body.
- If the **trailer** is present, add a blank line between the **body** and the **trailer**.

Mandatory:

- Answer as Markdown source in a code block.
- Trim whitespace at the start/end of the commit message.
