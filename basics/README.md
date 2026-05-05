# 🧾 Git Basics – Commands & Core Concepts

This section covers the **fundamental Git commands and concepts**, based on:

* CS50 Web Programming (Harvard)
* Git Learning PPT

---

# 📌 1. Repository (Repo)

A **repository** is a folder that contains:

* Project files
* Commit history

👉 It can be:

* Local (on your computer)
* Remote (on GitHub)

📖 A repository stores all files related to a project 

---

# 📌 2. Initialize Repository

```bash
git init
```

👉 Creates a new Git repository in your project folder

---

# 📌 3. Clone Repository

```bash
git clone <repository_url>
```

👉 Creates a copy of a remote repository on your computer

📖 Clone = copy from remote to local 

---

# 📌 4. Git Configuration

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

👉 Sets your identity for commits

---

# 📌 5. Git Status

```bash
git status
```

👉 Shows:

* Modified files
* Staged files
* Untracked files

📖 Used to check current repository state 

---

# 📌 6. Adding Files (Staging Area)

```bash
git add <file_name>
git add .
```

👉 Moves files to staging area

📖 Staging prepares files for commit 

---

# 📌 7. Commit Changes

```bash
git commit -m "message"
```

👉 Saves snapshot of your code

📖 Commit = snapshot of your project 

---

# 📌 8. Commit Shortcut

```bash
git commit -am "message"
```

👉 Adds + commits in one step
👉 Works only for tracked files

📖 Mentioned in CS50 notes 

---

# 📌 9. View Commit History

```bash
git log
```

👉 Shows:

* Commit ID
* Author
* Date
* Message

📖 Displays history of commits 

---

# 📌 10. Working with Files

## Create File

```bash
touch file.txt
```

## View Files

```bash
ls
```

## Change Directory

```bash
cd <folder_name>
```

👉 These are basic terminal commands used with Git

📖 Used in CS50 workflow steps 

---

# 📌 11. Git Lifecycle

```text
Working Directory → Staging Area → Repository
```

👉 Flow:

1. Modify file
2. Add file
3. Commit changes

---

# 📌 12. Key Concepts Summary

* Repository → Project folder
* Commit → Snapshot
* Staging → Preparing changes
* Clone → Copy repo
* Status → Check changes

---

# 🎯 Conclusion

These commands form the **foundation of Git** and are required before learning:

* Branching
* Merging
* Remote collaboration
