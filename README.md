# 🚀 Git & GitHub – Complete Notes (CS50 + PPT)

This repository contains my **complete notes and hands-on practice on Git & GitHub**, based strictly on:

* CS50 Web Programming (Harvard)
* Git Learning PPT (Beginner → Advanced)

---

# 📌 Repository Structure

This repo is organized into clear sections for better learning:

```bash
git-github-notes/
│
├── basics/            # Core concepts and commands
│   └── README.md
│
├── branching/         # Branching, merging, conflicts
│   └── README.md
│
├── practice/          # Real workflows + hands-on usage
│   ├── README.md
│   └── git-flow.md    # Step-by-step command flow
│
└── README.md          # Main overview (this file)
```

---

# 📚 Navigate Sections

👉 Start learning from here:

* 📘 [Basics](basics/README.md) → Fundamental Git concepts
* 🌿 [Branching](branching/README.md) → Deep understanding of branches & merge
* 💻 [Practice](practice/README.md) → Real-world workflows
* ⚡ [Git Flow Reference](practice/git-flow.md) → Quick command guide

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

```bash
Working Directory → Staging Area → Repository
```

## Commands:

```bash
git add <file>
git commit -m "message"
git push origin <branch>
```

---

# 🧾 4. Basic Commands

## Initialize Repository

```bash
git init
```

## Add Files

```bash
git add <file_name>
git add .
```

## Commit Changes

```bash
git commit -m "initial commit"
```

## Check Status

```bash
git status
```

## View History

```bash
git log
```

---

# 🌍 5. Working with Remote Repositories

## Clone Repository

```bash
git clone <repository_url>
```

## Push Changes

```bash
git push origin <branch_name>
```

## Pull Changes

```bash
git pull origin <branch_name>
```

👉 Used to sync between local and remote repositories

---

# 🌿 6. Branching & Merging

## Create Branch

```bash
git branch <branch_name>
```

## Switch Branch

```bash
git checkout <branch_name>
```

## Create & Switch

```bash
git checkout -b <branch_name>
```

## Merge Branch

```bash
git merge <branch_name>
```

## Delete Branch

```bash
git branch -d <branch_name>
```

👉 Branching allows working on new features without affecting main code

---

# ⚠️ 7. Merge Conflicts

Occurs when:

* Two changes conflict in same file

## Resolution:

```bash
git add <resolved_file>
git commit -m "Resolved conflict"
```

👉 Must be resolved manually

---

# 🔄 8. Undo Changes

## Undo Last Commit (keep changes)

```bash
git reset --soft HEAD~1
```

## Undo Last Commit (delete changes)

```bash
git reset --hard HEAD~1
```

## Discard Changes

```bash
git checkout -- <file_name>
```

---

# 🚀 9. Advanced Git

## Stash Changes

```bash
git stash
git stash pop
```

## Rebase

```bash
git rebase main
```

## Cherry Pick

```bash
git cherry-pick <commit_hash>
```

## Tagging

```bash
git tag -a v1.0 -m "version 1.0"
git push --tags
```

## Amend Commit

```bash
git commit --amend -m "new message"
```

---

# 🧹 10. Cleaning Repository

## Remove untracked files

```bash
git clean -f
```

## Remove directories

```bash
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

```bash
git rebase -i HEAD~3
```

## Submodules

```bash
git submodule add <repo_url>
git submodule update --init --recursive
```

## Bisect

```bash
git bisect start
git bisect bad
git bisect good <commit_hash>
```

## Aliases

```bash
git config --global alias.st status
```

---

# 💼 Author

**Pujitha Reddy**

---

⭐ This repository is structured for **step-by-step learning + real-world practice**
