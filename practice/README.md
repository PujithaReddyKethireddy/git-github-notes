# 💻 Git Practice – Real Workflow & Commands

This section focuses on **practical usage of Git commands and real-world workflows**, based on:

* CS50 Web Programming (Harvard)
* Git Learning PPT
* Hands-on practice

Unlike theoretical sections, this part demonstrates **how Git is actually used in day-to-day development**.

---

# 📌 1. Clone Repository (Starting a Project)

```bash id="d2a9c1"
git clone <repository_url>
cd <repository_name>
```

Cloning is usually the first step when working on an existing project. It creates a **local copy of a remote repository**, including all files and commit history.

👉 After cloning:

* You are connected to the remote repository
* You can start making changes immediately

📖 From CS50:
Cloning allows you to work locally while staying connected to the remote project.

---

# 📌 2. Creating and Modifying Files

```bash id="f8b2m6"
touch file.txt
```

This command creates a new file. After creating or modifying files, Git does not automatically track changes—you must explicitly add them.

👉 This step represents the **working directory stage**, where development happens.

---

# 📌 3. Checking Repository Status

```bash id="p4k9x7"
git status
```

This command provides a **snapshot of the current repository state**.

It shows:

* Untracked files (new files)
* Modified files (changed but not staged)
* Staged files (ready to commit)

👉 Developers frequently use this command to avoid mistakes.

---

# 📌 4. Adding Files to Staging

```bash id="z6y3q8"
git add file.txt
git add .
```

Before committing, Git requires you to **select which changes to include**.

* `git add file.txt` → adds a specific file
* `git add .` → adds all changes

👉 This step moves changes into the **staging area**, which acts like a preparation zone.

---

# 📌 5. Committing Changes

```bash id="x1c7r5"
git commit -m "Added file"
```

A commit is a **snapshot of your project at a specific point in time**.

👉 Good commit messages are important:

* Describe what changed
* Help track project history

📖 From CS50:
Each commit represents a saved version of your code.

---

# 📌 6. Pushing to GitHub

```bash id="v9t2n3"
git push origin main
```

This command uploads your commits from the **local repository to the remote repository (GitHub)**.

👉 After pushing:

* Your changes are visible online
* Other developers can access them

---

# 📌 7. Pulling Latest Changes

```bash id="q3p8m4"
git pull origin main
```

This command retrieves updates from the remote repository and merges them into your local project.

👉 This is important when:

* Working in a team
* Ensuring your code is up to date

---

# 📌 8. Full Beginner Workflow

```bash id="n7k2v1"
git clone <repo>
cd repo

touch file.txt

git add .
git commit -m "First commit"

git push origin main
```

This represents the **basic lifecycle of Git usage**:

* Create → Add → Commit → Push

---

# 📌 9. Branch Workflow (Real Development)

```bash id="h5x9c2"
git checkout -b feature1

# make changes

git add .
git commit -m "Feature added"

git push origin feature1

git checkout main
git merge feature1
```

In real-world development:

* Each feature is built in a separate branch
* Changes are merged into the main branch later

📖 From CS50:
Branching enables independent feature development.

---

# 📌 10. Merge Conflict Practice

A merge conflict occurs when Git cannot automatically combine changes.

```bash id="r4m8z6"
git pull
```

If a conflict exists:

* Git will mark conflicting sections in the file
* You must manually resolve them

After resolving:

```bash id="k2w7q3"
git add file.txt
git commit -m "Resolved conflict"
```

👉 This finalizes the merge.

---

# 📌 11. Reset Practice (Undo Changes)

## Soft Reset

```bash id="c8p1v9"
git reset --soft HEAD~1
```

* Removes last commit
* Keeps changes in staging

## Hard Reset

```bash id="b6x4m2"
git reset --hard HEAD~1
```

* Deletes commit and changes completely

⚠️ Use hard reset carefully.

---

# 📌 12. Viewing History

```bash id="t9f2k8"
git log
git log --oneline
```

These commands show:

* Commit history
* Messages
* Timeline of changes

👉 Useful for debugging and tracking progress.

---

# 📌 13. Comparing Changes

```bash id="j3k6m7"
git diff
```

This command shows **exact differences between file versions**.

👉 Useful before committing changes.

---

# 📌 14. Stash (Temporary Storage)

```bash id="u7p3n1"
git stash
git stash pop
```

Stash temporarily saves uncommitted changes.

👉 Use when:

* Switching branches
* Pausing work

---

# 📌 15. Cleaning Untracked Files

```bash id="l4w2x6"
git clean -f
```

Removes files that are not tracked by Git.

👉 Helps maintain a clean repository.

---

# 📌 16. Real Developer Workflow (IMPORTANT)

```bash id="e2y8n4"
git pull

# make changes

git add .
git commit -m "Updated feature"

git push
```

👉 This is the most commonly used workflow in teams.

---

# 📌 17. Common Mistakes

* Forgetting `git add` before commit
* Not pulling before pushing
* Using `git reset --hard` carelessly
* Ignoring `git status`

👉 These mistakes can lead to data loss or conflicts.

---

# 🎯 Conclusion

This section demonstrates:

* Real Git usage
* Practical workflows
* Command execution in real scenarios

👉 Mastering this section ensures you are ready for:

* Real-world development
* Team collaboration
* Technical interviews
