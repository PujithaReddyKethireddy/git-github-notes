# 🧾 Git Basics – Commands & Core Concepts

This section provides a **detailed understanding of fundamental Git concepts and commands**, based on:

* CS50 Web Programming (Harvard)
* Git Learning

These concepts form the **foundation of version control**, and understanding them clearly is essential before moving to advanced topics like branching and collaboration.

---

# 📌 1. Repository (Repo)

A **repository (repo)** is the core unit of Git. It is a folder that contains not only your project files but also the complete history of changes made to those files over time.

There are two types of repositories:

* **Local Repository**: Stored on your computer, where you write and modify code.
* **Remote Repository**: Stored on platforms like GitHub, used for sharing and collaboration.

In simple terms, a repository is like a **project folder with memory** — it remembers every change you make.

---

# 📌 2. Initialize Repository

```bash
git init
```

The `git init` command is used to **convert a normal folder into a Git repository**. It creates a hidden `.git` directory, which is where Git stores all version history and metadata.

Once initialized, Git starts tracking changes inside that folder.

👉 Use this when starting a project from scratch.

---

# 📌 3. Clone Repository

```bash
git clone <repository_url>
```

Cloning is used to **download an existing project from a remote repository (like GitHub)** to your local machine.

This command:

* Copies all files
* Copies entire commit history
* Connects your local repo to the remote repo

👉 After cloning, you usually run:

```bash
cd <repository_name>
```

This allows you to start working on the project immediately.

---

# 📌 4. Git Configuration

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Git requires your identity because every commit stores:

* Author name
* Author email

These details help track **who made which change**, especially in collaborative projects.

👉 The `--global` flag applies this configuration to all repositories on your system.

---

# 📌 5. Git Status

```bash
git status
```

This is one of the **most important commands in Git**.

It shows:

* Modified files (changed but not staged)
* Staged files (ready to commit)
* Untracked files (new files not yet tracked by Git)

👉 You should use `git status` frequently to understand the current state of your project.

---

# 📌 6. Adding Files (Staging Area)

```bash
git add <file_name>
git add .
```

Before saving changes, Git requires you to **select which files should be included in the next commit**. This process is called **staging**.

* `git add <file_name>` → adds a specific file
* `git add .` → adds all modified files

The staging area acts like a **preview zone** before committing changes.

---

# 📌 7. Commit Changes

```bash
git commit -m "message"
```

A commit is a **snapshot of your project at a specific point in time**.

* It saves all staged changes
* It creates a permanent record in Git history

The message should describe **what changes were made and why**.

👉 Example:

```bash
git commit -m "Added login functionality"
```

---

# 📌 8. Commit Shortcut

```bash
git commit -am "message"
```

This command is a shortcut that:

* Adds all **already tracked files**
* Commits them in one step

⚠️ Important:
It does **NOT include new (untracked) files**

---

# 📌 9. View Commit History

```bash
git log
```

This command displays the **history of all commits** in the repository.

Each commit includes:

* Commit ID (unique hash)
* Author name
* Date and time
* Commit message

👉 This helps you:

* Track changes
* Debug issues
* Revert to previous versions

---

# 📌 10. Working with Files (Terminal Basics)

These are basic commands used alongside Git:

### Create a file

```bash
touch file.txt
```

### List files

```bash
ls
```

### Change directory

```bash
cd <folder_name>
```

These commands are part of the normal development workflow and are often used in Git-based projects.

---

# 📌 11. Git Lifecycle (Core Concept)

```text
Working Directory → Staging Area → Repository
```

Git operates in three main stages:

1. **Working Directory**

   * Where you edit files

2. **Staging Area**

   * Where you prepare changes

3. **Repository**

   * Where commits are stored permanently

👉 Flow:

* Modify file
* Add to staging
* Commit changes

This lifecycle is the **heart of Git**.

---

# 📌 12. Key Concepts Summary

* **Repository** → Project folder with history
* **Commit** → Snapshot of code
* **Staging** → Preparing changes before saving
* **Clone** → Copy remote repository
* **Status** → Check current changes

---

# 🎯 Conclusion

These basic commands and concepts form the **foundation of Git**.

Understanding them clearly allows you to:

* Track changes effectively
* Manage project history
* Prepare for advanced topics like:

  * Branching
  * Merging
  * Remote collaboration

👉 Mastering these basics is essential before moving forward.
