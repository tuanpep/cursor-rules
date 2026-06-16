# cursor-rules

Shared [Cursor project rules](https://cursor.com/docs/rules) for disciplined AI-assisted coding. Import into any project via **Remote Rule (GitHub)** or copy individual `.mdc` files.

## Import via GitHub

1. Open **Cursor Settings → Rules, Commands**
2. Click **+ Add Rule** next to Project Rules → **Remote Rule (GitHub)**
3. Paste this repository URL:

   ```
   https://github.com/tuanpep/cursor-rules
   ```

4. Cursor scans all `.mdc` files under `rules/` and syncs them into your project at `.cursor/rules/imported/cursor-rules/`.

Rules keep their relative paths, so `rules/verification-loop.mdc` becomes `.cursor/rules/imported/cursor-rules/rules/verification-loop.mdc`.

Private repos work if your GitHub account has access.

## Manual install

Copy the rules you want into your project's `.cursor/rules/`:

```bash
cp rules/verification-loop.mdc /path/to/your-project/.cursor/rules/
```

## Rules

| Rule | Apply mode | Scope |
|------|------------|-------|
| [verification-loop](rules/verification-loop.mdc) | Always | Prove changes with lint, test, or build before claiming done |
| [bounded-autonomy](rules/bounded-autonomy.mdc) | Always | Act freely on safe work; ask before risky actions |
| [task-scope](rules/task-scope.mdc) | Always | Match planning effort to task risk |
| [anti-vibe-coding](rules/anti-vibe-coding.mdc) | Always | Understand and verify code; never ship unread output |
| [ai-smell](rules/ai-smell.mdc) | Always | Self-check for plausible-but-wrong AI output |
| [context-management](rules/context-management.mdc) | Always | Optimize context window usage and prevent context rot |
| [agentic-pr](rules/agentic-pr.mdc) | Always | Formulate atomic commits and summaries to prevent review fatigue |
| [coding-principles](rules/coding-principles.mdc) | Always | Scope, conventions, comments, tests |
| [kiss](rules/kiss.mdc) | Always | Keep implementations simple |
| [yagni](rules/yagni.mdc) | Always | Build only what was asked |
| [local-reasoning](rules/local-reasoning.mdc) | Always | Write code understandable in isolation |
| [error-handling](rules/error-handling.mdc) | Always | Handle exceptions explicitly and fail fast and loud |
| [evolutionary-change](rules/evolutionary-change.mdc) | Always | Refactor safely using Parallel Change |
| [agentic-security](rules/agentic-security.mdc) | Always | Implement input validation, output encoding, and protect secrets |

All rules apply globally across all programming languages and file extensions.

## Updating

After you push changes to this repo, re-sync from **Cursor Settings → Rules** to pull updates into imported projects.
