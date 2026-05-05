# 🚀 Git Command Flow (Step-by-Step Reference)

This is a **complete Git workflow** from project start → collaboration → advanced usage.

---

# 📌 1. FIRST TIME SETUP (One-time only)

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git --version
```

---

# 📌 2. CREATE OR CLONE REPOSITORY

## 🔹 Option A: Clone existing repo

```bash
git clone <repository_url>
cd <repository_name>
```

## 🔹 Option B: Create new repo

```bash
git init
git remote add origin <repository_url>   # connect to GitHub
git remote -v                            # verify remote
```

---

# 📌 3. CHECK STATUS & DIFFERENCES

```bash
git status              # current state
git diff                # show changes before commit
```

---

# 📌 4. ADD FILES (STAGING)

```bash
git add file.txt        # add specific file
git add .               # add all files
```

---

# 📌 5. COMMIT CHANGES

```bash
git commit -m "message"
git commit -am "message"   # shortcut (tracked files only)
```

---

# 📌 6. FIRST PUSH (SET UPSTREAM)

```bash
git push -u origin main
```

👉 After this:

```bash
git push
```

---

# 📌 7. BASIC WORKFLOW (MOST USED 🔥)

```bash
git status
git add .
git commit -m "message"
git push
```

---

# 📌 8. DAILY WORKFLOW (IMPORTANT)

```bash
git pull                # get latest changes

# make changes

git add .
git commit -m "updated code"

git push
```

👉 Rule:
👉 **pull → work → add → commit → push**

---

# 📌 9. BRANCH WORKFLOW (REAL DEVELOPMENT)

```bash
git branch                  # view branches
git checkout -b feature1   # create branch
git checkout main          # switch branch
```

```bash
# make changes

git add .
git commit -m "feature added"

git push origin feature1
```

---

# 📌 10. MERGE WORKFLOW

```bash
git checkout main
git pull
git merge feature1
```

---

# 📌 11. MERGE CONFLICT RESOLUTION

```bash
# fix file manually

git add <file>
git commit -m "resolved conflict"
```

---

# 📌 12. VIEW HISTORY

```bash
git log
git log --oneline
git log --oneline --graph   # visual history 🔥
```

---

# 📌 13. WORKING WITH REMOTE

```bash
git fetch origin      # download only
git pull              # download + merge
git push              # upload
```

---

# 📌 14. UNDO CHANGES

## Undo last commit (keep changes)

```bash
git reset --soft HEAD~1
```

## Undo last commit (delete changes)

```bash
git reset --hard HEAD~1
```

## Reset to remote version

```bash
git reset --hard origin/main
```

---

# 📌 15. STASH (TEMP SAVE WORK)

```bash
git stash
git stash pop
```

---

# 📌 16. CLEAN REPOSITORY

```bash
git clean -f
git clean -fd
```

---

# 📌 17. ADVANCED COMMANDS

```bash
git rebase main
git cherry-pick <commit>
git tag -a v1.0 -m "version"
git push --tags
```

---

# 📌 18. COMPLETE REAL WORKFLOW (FINAL)

```bash
git clone <repo>
cd repo

git checkout -b feature

# work

git add .
git commit -m "feature added"

git push origin feature

git checkout main
git pull
git merge feature

git push
```

---

# 📌 19. EXTRA IMPORTANT COMMANDS (🔥 ADDED)

## Delete branch after merge

```bash
git branch -d feature1
```

## Restore file changes

```bash
git restore file.txt
git restore --staged file.txt
```

## .gitignore (ignore files)

```bash
touch .gitignore
```

👉 Used to ignore:

* node_modules
* temp files
* secrets

---

# 🎯 FINAL RULE (IMPORTANT)

```bash
git pull → work → git add → git commit → git push
```

---

# 💡 SUMMARY

* git add → stage
* git commit → save
* git push → upload
* git pull → sync
* git merge → combine
* git diff → check changes
* git branch → view branches
* git remote → connect repo

---

⭐ This file is your **daily Git reference**
