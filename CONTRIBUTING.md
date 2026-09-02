# Contributing to the Nexus Docs

Nexus's application source code is closed and proprietary — this repository covers documentation only. Contributions here are welcome and handled differently from a typical open-source project as a result.

## What You Can Contribute

- Fixes for inaccurate, outdated, or unclear documentation
- Clarifications based on real user confusion (if something in [Getting Started](docs/getting-started.md) or the [FAQ](docs/faq.md) didn't make sense to you, others likely hit the same thing)
- Typo and formatting fixes
- New FAQ entries for questions that keep coming up in issues or support

## What This Repo Is Not For

- Bug reports about the Nexus application itself — use the main [issue tracker](#)
- Feature requests for the app — use the main [issue tracker](#)
- Source code, build instructions, or anything about the app's internal implementation — Nexus does not accept or host external code contributions, since the codebase itself is not public

## Making a Change

1. Fork this repository.
2. Make your edit. Keep the existing tone: direct, accurate, and free of marketing language — describe what Nexus actually does, not what it aspires to do.
3. Open a pull request with a short description of what changed and why.

Small, focused pull requests (one fix or one addition) are easier to review and merge than large rewrites.

## Style Notes

- Use `##`/`###` headings consistently with the existing files rather than introducing new heading levels.
- Prefer short paragraphs and tables over long prose where a comparison is being made.
- Don't add screenshots or images without confirming the current UI matches — Nexus changes over time, and a stale screenshot is worse than none.
- Every claim about what data is or isn't sent somewhere must be accurate — when in doubt, open an issue asking for clarification rather than guessing.
