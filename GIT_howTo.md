## VIM
write commit
esc
:wq ( write and quit)


## ✅ 1. Initialize Git in a new local project

**When:** You just created a new local project folder and want to start version control.

```bash
git init
git add .
git commit -m "Initial commit"
```

---

## ✅ 2. Create `README.md` to include in first commit

**When:** You want a README file before pushing to GitHub.

```bash
echo "# Project Title" > README.md
git add README.md
git commit -m "Add README"
```

---

## ✅ 3. Rename default branch to `main`

**When:** Your local repo uses `master` and you want it to be `main`.

```bash
git branch -M main
```

---

## ✅ 4. Connect to a remote GitHub repository

**When:** You have created a GitHub repo and want to push your local project to it.

```bash
git remote add origin https://github.com/yourusername/repo-name.git
```

---

## ✅ 5. Push to GitHub (initial push, no remote content)

**When:** You created an empty GitHub repo (no README, no .gitignore, etc.).

```bash
git push -u origin main
```

---

## ❗ 6. Push to GitHub (but remote repo already has README/.gitignore)

**When:** Local and remote have separate history (e.g., both `git init` separately).

```bash
git pull origin main --allow-unrelated-histories
git add .
git commit -m "Merge remote and local histories"
git push
```

---

## ❗ 7. Fix "refusing to merge unrelated histories"

**When:** Git blocks pull due to different repo histories.

```bash
git pull origin main --allow-unrelated-histories
```

---

## ❗ 8. Set tracking between local and remote branches

**When:** You see “no tracking information” error when pulling or pushing.

```bash
git branch --set-upstream-to=origin/main main
```

_or pull and set tracking in one:_

```bash
git pull --set-upstream origin main
```

---

## ✅ 9. Clone an existing repository

**When:** You want to copy a GitHub repo to your computer.

```bash
git clone https://github.com/username/repo-name.git
```

---

## ✅ 10. Create and switch to a new branch

**When:** You want to start a new feature or isolate changes.

```bash
git checkout -b feature/my-feature
```

---

## ✅ 11. Switch to another existing branch

**When:** You want to go back to an existing branch.

```bash
git checkout main
```

---

## ✅ 12. Merge a branch into another

**When:** You want to apply changes from one branch to another.

```bash
git checkout main
git merge feature/my-feature
```

---

## ✅ 13. Push a new branch to GitHub

**When:** You created a new branch locally and want to push it.

```bash
git push -u origin feature/my-feature
```

---

## ✅ 14. Pull latest changes from the remote

**When:** You want to sync your local branch with GitHub.

```bash
git pull
```

---

## ✅ 15. Check current branch and status

**When:** You want to check which branch you’re on and what's changed.

```bash
git branch
git status
```

---

## ✅ 16. See commit history

**When:** You want to review past commits.

```bash
git log
```

---

## ✅ 17. Stage specific files only

**When:** You don’t want to stage everything at once.

```bash
git add filename.txt
```

---

## ✅ 18. Remove a file from Git tracking (but keep it locally)

**When:** You want to ignore a committed file without deleting it.

```bash
git rm --cached filename.txt
```

---

## 🔧 Common Git flags

| Flag | Meaning | Example |
|------|---------|---------|
| `-m` | Message | `git commit -m "Initial commit"` |
| `-M` | Rename branch | `git branch -M main` |
| `-u` | Set upstream (link local to remote branch) | `git push -u origin main` |
| `--set-upstream` | Same as `-u` | `git pull --set-upstream origin main` |
| `--allow-unrelated-histories` | Merge unrelated histories | `git pull origin main --allow-unrelated-histories` |

---

## 📝 Exit Git's text editor (Vim)

When Git opens a text editor (e.g. for merge or commit messages):

### Save and exit:
```vim
ESC
:wq
ENTER
```

### Exit without saving:
```vim
ESC
:q!
ENTER
```

---

## 💡 Optional: Use Notepad as Git editor (on Windows)
```bash
git config --global core.editor "notepad"
```

---

