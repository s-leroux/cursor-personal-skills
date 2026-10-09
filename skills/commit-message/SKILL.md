---
name: commit-message
description: Propose a short git commit title and body from staged and working-tree changes. Use when the user invokes /commit-message.
disable-model-invocation: true
metadata:
  version: "1.1.0"
---

Propose a short commit title + body message for the changes (staged and in the working tree).

Identification/best-effort:

- Inspect the previous commit messages to find a pattern and reuse it if possible (style, length, etc.).
- Identify if the commit is stand-alone or part of a larger feature/bugfix commit chain.
- Look at the **branch name** and related **issue** to find clues about the **purpose** of the commit.
- Identify the **implementation details** using the **commit history**, the **codebase**, and **diff tools**.
- Ignore the untracked files in the working tree.

Rules:

- The commit **title** should be a single line of text focusing on the **purpose** of the commit.
- The commit **title** start with an action verb (e.g. `Add`, `Fix`, `Refactor`, `Update`, `Remove`, `Move`, `Rename`, `Change`, `Improve`, `Optimize`, `Simplify`, `Refine`, ...).
- The commit **title** should be 50 characters or less.
- If the commit is a typo fix or similar minor change, leave the **body** empty.
- Otherwise, add one blank line between the **title** and the **body**.
- If present, the **body**:
  - Should be a single paragraph when the diff is one change.
  - Should be a list of bullet points (with a leading `- `) when the diff contains several distinct changes with different purposes. One bullet per change, each focused on the purpose of that change.
  - **Implementation details**, if necessary, follow the paragraph or the list as individual paragraphs.
  - Paragraphs should be separated by a blank line.
  - In all cases, body lines should be wrapped at 72 characters.
    No early break at less than 67 characters.
- If the commit is an obvious fix for a registered issue, add `Close #<issue-number>` or `Fix #<issue-number>` as a **trailer** after the body.
- If the **trailer** is present, add a blank line between the **body** and the **trailer**.

Mandatory:

- Answer as Markdown source in a code block.
- Trim whitespace at the start/end of the commit message.
