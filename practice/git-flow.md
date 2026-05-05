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

Cloning creates a **local copy of a remote repository**, including all files and commit history.

👉 After cloning:

* You are connected to the remote repository
* You can start working immediately

---

# 📌 2. Creating and Modifying Files

```bash id="f8b2m6"
touch file.txt
```

Creates a new file. Git does not track changes automatically—you must explicitly add them.

👉 This represents the **working directory stage**, where development happens.

---

# 📌 3. Checking Repository Status

```bash id="p4k9x7"
git status
```

Shows the current state of your project:

* Untracked files
* Modified files
* Staged files

👉 Always run this before committing to avoid mistakes.

---

# 📌 4. Adding Files to Staging

```bash id="z6y3q8"
git add file.txt
git add .
```

Moves changes to the **staging area**.

* Specific file → `git add file.txt`
* All files → `git add .`

👉 Staging allows you to control what goes into the next commit.

---

# 📌 5. Committing Changes

```bash id="x1c7r5"
git commit -m "Added file"
```

Creates a **snapshot of your project**.

👉 Good commit messages:

* Clearly describe the change
* Make history easy to understand

---

# 📌 6. Pushing to GitHub

```bash id="v9t2n3"
git push origin main
```

Uploads your changes to GitHub.

👉 **Pro Tip:**

```bash id="z4j9c2"
git push -u origin main
```

* Sets upstream branch
* After this → simply use:

```bash id="j3x7k1"
git push
```

---

# 📌 7. Pulling Latest Changes

```bash id="q3p8m4"
git pull origin main
```

Downloads and merges updates from GitHub.

👉 Always pull before starting work to avoid conflicts.

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

👉 Flow:
Create → Add → Commit → Push

---

# 📌 9. Branch Workflow (Real Development)

```bash id="h5x9c2"
git checkout -b feature1

# make changes

git add .
git commit -m "Feature added"

git push -u origin feature1
```

```bash id="k8d2m7"
git checkout main
git pull
git merge feature1
```

👉 Features should always be developed in separate branches.

---

# 📌 10. Merge Conflict Practice

```bash id="r4m8z6"
git pull
```

If a conflict occurs:

* Git marks conflicting sections in the file
* You must resolve them manually

```bash id="k2w7q3"
git add file.txt
git commit -m "Resolved conflict"
```

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

⚠️ Use `--hard` carefully — it permanently deletes work.

---

# 📌 12. Viewing History

```bash id="t9f2k8"
git log
git log --oneline
git log --oneline --graph --all
```

👉 Shows:

* Commit history
* Branch structure
* Merge relationships

---

# 📌 13. Comparing Changes

```bash id="j3k6m7"
git diff              # unstaged changes
git diff --staged     # staged changes
```

👉 Helps verify changes before committing.

---

# 📌 14. Stash (Temporary Storage)

```bash id="u7p3n1"
git stash
git stash pop
```

Temporarily saves uncommitted changes.

👉 Useful when:

* Switching branches
* Handling urgent tasks

---

# 📌 15. Cleaning Untracked Files

```bash id="l4w2x6"
git clean -f
```

Removes untracked files.

⚠️ This cannot be undone — use carefully.

---

# 📌 16. Real Developer Workflow (IMPORTANT)

```bash id="e2y8n4"
git pull

# make changes

git add .
git commit -m "Updated feature"

git push
```

👉 Golden rule:
👉 **pull → work → add → commit → push**

---

# 📌 17. Amend Commit (Fix Last Commit)

```bash id="p9x4v2"
git commit --amend -m "Updated message"
```

👉 Use when:

* You forgot to include a file
* You want to fix the commit message

⚠️ Avoid using after pushing (rewrites history).

---

# 📌 18. Common Mistakes

* Forgetting `git add`
* Not pulling before pushing
* Using `git reset --hard` carelessly
* Ignoring `git status`

👉 These mistakes can lead to conflicts or data loss.

---

# 🎯 Conclusion

This section demonstrates:

* Real Git usage
* Practical workflows
* Command execution in real scenarios

👉 Mastering this ensures you are ready for:

* Real-world development
* Team collaboration
* Technical interviews
