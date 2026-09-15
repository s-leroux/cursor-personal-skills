---
name: xxx-to-github-issues
description: Convert `XXX` comments into tracked GitHub issues and re-point the source comments at those issues. Use when the user asks to convert XXX comments, open issues from XXX notes, or re-point comments at GitHub issues.
---

Comments marked `XXX` record issues noticed while implementing other
work. Convert them into tracked GitHub issues and re-point the comments
at those issues.

1. **Collect** every `XXX` comment in the repository. Ignore false
   positives (for example `XXXXX` as an API-token placeholder in a URL).
2. **Deduplicate** notes that describe the same problem or existing GitHub issues. Keep file and
   line references (and a short code fragment) for each occurrence.
3. **Open one GitHub issue per unique new problem.** Each issue should have
   a concise title, a short description, the relevant code fragment(s),
   and labels consistent with the repository’s existing taxonomy.
4. **Rewrite the source comments:** replace every marker matching
   `/XXX:?/` with `ISSUE #nn:`, where `nn` is the newly assigned issue
   number. Leave the rest of the comment unchanged, aside from minor
   orthographic corrections.

Do not commit unless explicitly asked.
