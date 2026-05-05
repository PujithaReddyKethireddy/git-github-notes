# 💻 Git Practice – Real Workflow & Commands

This section contains **practical Git workflows and real command usage**, based on:

* CS50 Web Programming (Harvard)
* Git Learning PPT

---

# 📌 1. Clone Repository (Start Project)

```bash id="k1a9m3"
git clone <repository_url>
cd <repository_name>
```

👉 Downloads repository and moves into project folder

📖 CS50: cloning creates a local copy of remote repository 

---

# 📌 2. Create File and Make Changes

```bash id="p3m8k1"
touch file.txt
```

👉 Create new file and edit it

---

# 📌 3. Check Status

```bash id="x7d9f2"
git status
```

👉 Shows:

* Untracked files
* Modified files

📖 PPT: used to check repository state 

---

# 📌 4. Add Files to Staging

```bash id="t8r1c6"
git add file.txt
git add .
```

👉 Moves files to staging area

---

# 📌 5. Commit Changes

```bash id="n2k7q5"
git commit -m "Added file"
```

👉 Saves snapshot of changes

📖 CS50: commit saves current state of code 

---

# 📌 6. Push to GitHub

```bash id="y6z2m8"
git push origin main
```

👉 Uploads changes to remote repository

📖 CS50: push updates GitHub repository 

---

# 📌 7. Pull Latest Changes

```bash id="v4c8x1"
git pull origin main
```

👉 Gets latest updates from GitHub

📖 Used when remote repo is ahead 

---

# 📌 8. Full Workflow (BEGINNER)

```bash id="z8t3k9"
git clone <repo>
cd repo

touch file.txt

git add .
git commit -m "First commit"

git push origin main
```

---

# 📌 9. Branch Workflow (REAL)

```bash id="f5w1n7"
git checkout -b feature1

# make changes

git add .
git commit -m "Feature added"

git push origin feature1

git checkout main
git merge feature1
```

📖 CS50: branching allows feature development separately 

---

# 📌 10. Merge Conflict Practice

When conflict happens:

```bash id="u3p6l4"
git pull
```

👉 File will show conflict markers

Fix manually, then:

```bash id="r9h2q8"
git add file.txt
git commit -m "Resolved conflict"
```

📖 Conflicts occur when two changes overlap 

---

# 📌 11. Reset Practice

## Soft Reset

```bash id="d6k1s2"
git reset --soft HEAD~1
```

## Hard Reset

```bash id="q7m4t8"
git reset --hard HEAD~1
```

📖 PPT: reset used to undo commits 

---

# 📌 12. View History

```bash id="l2c8v5"
git log
git log --oneline
```

👉 Shows commit history

---

# 📌 13. Compare Changes

```bash id="w9f3n6"
git diff
```

👉 Shows differences between changes

📖 PPT: used for comparing code changes 

---

# 📌 14. Stash Practice

```bash id="m1r7p4"
git stash
git stash pop
```

👉 Temporarily saves changes

📖 PPT: used to store unfinished work 

---

# 📌 15. Clean Untracked Files

```bash id="c3x9z2"
git clean -f
```

👉 Removes untracked files

📖 PPT: used to clean repository 

---

# 📌 16. Real Developer Workflow (IMPORTANT)

```bash id="g8k2n5"
git pull

# make changes

git add .
git commit -m "Updated feature"

git push
```

👉 Always pull before push

---

# 📌 17. Common Mistakes

❌ Forgetting `git add`
❌ Not pulling before pushing
❌ Using `git reset --hard` carelessly
❌ Not checking `git status`

---

# 🎯 Conclusion

This section demonstrates:

* Real Git usage
* Complete workflows
* Practical commands

👉 This is what makes you **job-ready**
