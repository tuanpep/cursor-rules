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
| [coding-principles](rules/coding-principles.mdc) | On matching files | Scope, conventions, comments, tests |
| [kiss](rules/kiss.mdc) | On matching files | Keep implementations simple |
| [yagni](rules/yagni.mdc) | On matching files | Build only what was asked |
| [local-reasoning](rules/local-reasoning.mdc) | On matching files | Write code understandable in isolation |

File-scoped rules auto-attach for `**/*.{ts,tsx,js,jsx}`.

## Updating

After you push changes to this repo, re-sync from **Cursor Settings → Rules** to pull updates into imported projects.
