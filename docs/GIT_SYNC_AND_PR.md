# Sync with remote and open a PR

Use this when someone else has pushed to the repo and you want your MacBook up to date, then contribute via a PR instead of pushing directly to main.

## Prompt for Cursor

Copy and paste this when you need to sync and prepare a PR:

```
Sync this repo with the remote: fetch origin, pull main so my working copy is up to date with the latest from GitHub. Then create a new branch for my changes (e.g. fix/docs-config or feature/whatever) so I can make edits and open a PR instead of pushing to main. Run the git commands and tell me the branch name to use for the PR.
```

Cursor will run the right `git fetch`, `git pull`, and `git checkout -b <branch>` (or equivalent) and remind you to push the branch and open a PR.

## Commands to run yourself

From the repo root (`LayoutDocs`):

```bash
# 1. Get latest from GitHub
git fetch origin
git pull origin main

# 2. Create a branch for your work (pick a short name)
git checkout -b fix/docs-config

# 3. Make your edits, then commit and push the branch
git add .
git commit -m "Your message"
git push -u origin fix/docs-config
```

Then on GitHub: open the repo → you’ll usually see “Compare & pull request” for the branch you just pushed → open the PR.

## If pull has conflicts

If `git pull origin main` reports conflicts:

```bash
git status   # see conflicted files
# Edit the files to resolve conflicts, then:
git add .
git commit -m "Merge main and resolve conflicts"
```

Then continue with your branch and push.
