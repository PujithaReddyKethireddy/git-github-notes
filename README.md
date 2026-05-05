# 🚀 Git & GitHub – Complete Notes (CS50 + PPT)

This repository contains my **complete notes and practice on Git & GitHub**, based strictly on:

* CS50 Web Programming (Harvard)
* Git Learning PPT (Beginner → Advanced)

---

# 📌 1. What is Git?

Git is a **distributed version control system** that helps:

* Track changes in code
* Save snapshots of projects
* Collaborate with multiple developers
* Revert to previous versions

👉 Git allows us to:

* Keep track of changes over time
* Synchronize code between different users
* Work on different branches without affecting main code
* Restore earlier versions if needed 

---

# 🌐 2. What is GitHub?

GitHub is a platform that:

* Stores Git repositories online
* Enables collaboration
* Allows pushing and pulling code

👉 A repository is:
A folder that contains all files of a project (local or remote) 

---

# ⚙️ 3. Git Workflow

```bash id="c4d0m3"
Working Directory → Staging Area → Repository
```

## Commands:

```bash id="f3s8m0"
git add <file>
git commit -m "message"
git push origin <branch>
```

---

# 🧾 4. Basic Commands

## Initialize Repository

```bash id="psr3e1"
git init
```

## Add Files

```bash id="8v06kj"
git add <file_name>
git add .
```

## Commit Changes

```bash id="8a8rmh"
git commit -m "initial commit"
```

## Check Status

```bash id="0b3q3x"
git status
```

## View History

```bash id="ghw0rf"
git log
```

---

# 🌍 5. Working with Remote Repositories

## Clone Repository

```bash id="m6m2we"
git clone <repository_url>
```

## Push Changes

```bash id="8t3csh"
git push origin <branch_name>
```

## Pull Changes

```bash id="s9sz1y"
git pull origin <branch_name>
```

👉 Used to sync between local and remote repositories 

---

# 🌿 6. Branching & Merging

## Create Branch

```bash id="dcnwzm"
git branch <branch_name>
```

## Switch Branch

```bash id="r6bm2y"
git checkout <branch_name>
```

## Create & Switch

```bash id="2lfmyd"
git checkout -b <branch_name>
```

## Merge Branch

```bash id="d3h3q7"
git merge <branch_name>
```

## Delete Branch

```bash id="9t6xcl"
git branch -d <branch_name>
```

👉 Branching allows working on new features without affecting main code 

---

# ⚠️ 7. Merge Conflicts

Occurs when:

* Two changes conflict in same file

## Resolution:

```bash id="2e7h3g"
git add <resolved_file>
git commit -m "Resolved conflict"
```

👉 Must be resolved manually 

---

# 🔄 8. Undo Changes

## Undo Last Commit (keep changes)

```bash id="dx1b0x"
git reset --soft HEAD~1
```

## Undo Last Commit (delete changes)

```bash id="7ix3u7"
git reset --hard HEAD~1
```

## Discard Changes

```bash id="6umz4j"
git checkout -- <file_name>
```

---

# 🚀 9. Advanced Git

## Stash Changes

```bash id="l4u6m3"
git stash
git stash pop
```

## Rebase

```bash id="0g9gkq"
git rebase main
```

## Cherry Pick

```bash id="q2hkgv"
git cherry-pick <commit_hash>
```

## Tagging

```bash id="5m6h7z"
git tag -a v1.0 -m "version 1.0"
git push --tags
```

## Amend Commit

```bash id="1c3e6h"
git commit --amend -m "new message"
```

---

# 🧹 10. Cleaning Repository

## Remove untracked files

```bash id="1g1y7c"
git clean -f
```

## Remove directories

```bash id="h9h1bz"
git clean -fd
```

---

# 🧠 11. Best Practices

* Write meaningful commit messages
* Commit frequently
* Keep branches small
* Sync regularly with main branch 

---

# 🔧 12. Expert Commands

## Interactive Rebase

```bash id="8fdwz8"
git rebase -i HEAD~3
```

## Submodules

```bash id="t9z5sj"
git submodule add <repo_url>
git submodule update --init --recursive
```

## Bisect

```bash id="8l2kfx"
git bisect start
git bisect bad
git bisect good <commit_hash>
```

## Aliases

```bash id="g9z5z9"
git config --global alias.st status
```

---

# 💼 Author

Pujitha Reddy
