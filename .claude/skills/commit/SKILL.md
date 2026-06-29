---
name: commit
description: Stage all changes and create a git commit with a message that summarizes them. Use when the user asks to commit their work, save changes to git, or says "/commit".
---

# Commit

Stage the current changes and commit them with a concise, accurate message summarizing what changed.

## Steps

1. Inspect the working tree before doing anything:
   - `git status` to see untracked and modified files.
   - `git diff` and `git diff --staged` to understand the actual content of the changes.
   - `git log --oneline -10` to match the repository's existing commit message style.

2. Stage the changes with `git add -A` (stage everything), unless the user named specific files — then stage only those.

3. Write a commit message that **summarizes the staged changes**:
   - A short imperative subject line (≈50 chars) describing the net effect, e.g. `Add outbox pattern note`.
   - If several unrelated things changed, add a brief body with one bullet per logical change.
   - Describe what the diff actually does — do not invent changes that aren't staged.

4. Create the commit. Use a heredoc so multi-line messages format correctly:

   ```bash
   git commit -m "$(cat <<'EOF'
   Subject line summarizing the change

   - optional detail bullet
   EOF
   )"
   ```

5. Confirm with `git status` and report the new commit (`git log --oneline -1`) back to the user.

## Notes

- This is a personal notes repo; keep messages plain and factual, matching the casual style of recent commits.
- Commit only — do **not** push unless the user explicitly asks.
- If there is nothing to commit, say so instead of creating an empty commit.