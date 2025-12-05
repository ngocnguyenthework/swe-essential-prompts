# auto-commit

Generate a commit message based on the provided diff.

Input:

- Diff:  
  [Paste diff here — if omitted, auto-detect from project]

Rules:

- Follow **Conventional Commits** format.
- The **commit message must clearly summarize the specific changes made**, including affected sections, files, or functionality.
- Avoid vague terms like "recent changes"; describe exactly what was added, updated, or removed.
- Produce a **single-line commit message** unless additional sections are explicitly requested.

Optional (include if user specifies):

- **Commit Body:** Explain _why_ the change was made and its potential impact.
- **PR Description:** Include summary, reasoning, and a standard checklist.
- **Changelog Entry:** Follows Keep a Changelog style.

Output:

- **Commit message (mandatory):** descriptive, concise, and specific.
- Additional sections (optional)
