# 🌿 Branching & Merging in Git

This section explains **branching, merging, and conflicts**, based on:

* CS50 Web Programming (Harvard)
* Git Learning PPT

---

# 📌 1. What is a Branch?

A **branch** is an independent line of development.

👉 It allows you to:

* Work on new features
* Fix bugs
* Experiment safely

📖 From CS50:
Branching lets us make changes **without affecting the main codebase**, and later merge them 

---

# 📌 2. Why Branching is Important

Without branching:

* All changes affect main code ❌

With branching:

* Work independently ✔
* Merge later ✔

📖 CS50 shows that branching helps avoid breaking the main project while developing features 

---

# 📌 3. Create a Branch

```bash id="5l9w2y"
git branch <branch_name>
```

👉 Creates a new branch

---

# 📌 4. Switch Branch

```bash id="z9j7yf"
git checkout <branch_name>
```

👉 Moves to that branch

---

# 📌 5. Create + Switch (Best Practice)

```bash id="3o8d8k"
git checkout -b <branch_name>
```

👉 Creates and switches in one command

📖 Recommended workflow from CS50 branching section 

---

# 📌 6. Check Current Branch

```bash id="e3d7sf"
git branch
```

👉 Shows all branches
👉 Current branch has `*`

📖 CS50: current branch is indicated with an asterisk 

---

# 📌 7. HEAD Concept (IMPORTANT)

👉 HEAD points to the current branch

* Default → main (or master)
* Changes when you switch branches

📖 CS50:
HEAD determines which branch you are currently working on 

---

# 📌 8. Merge Branch

```bash id="b8r3wx"
git checkout main
git merge <branch_name>
```

👉 Combines branch into main

📖 Merging integrates feature branch into main project 

---

# 📌 9. Delete Branch

```bash id="8q1p2k"
git branch -d <branch_name>
```

👉 Removes branch after merging

📖 Mentioned in PPT branching section 

---

# 📌 10. Merge Conflict (VERY IMPORTANT)

Occurs when:

* Same part of file changed differently

---

## 🔹 Example (from CS50)

```bash id="b2y6qk"
<<<<<<< HEAD
b = 2
=======
b = 3
>>>>>>> commit
```

📖 Conflict markers shown when merging changes 

---

# 📌 11. Resolve Conflict

Steps:

1. Open file
2. Choose correct code
3. Remove markers
4. Run:

```bash id="9e2f1p"
git add <file>
git commit -m "Resolved conflict"
```

📖 PPT confirms manual resolution + commit 

---

# 📌 12. Branch Workflow (REAL)

```bash id="6k2m4y"
git checkout -b feature-login

# make changes

git add .
git commit -m "Added feature"

git checkout main
git merge feature-login
```

---

# 📌 13. Key Concepts Summary

* Branch → separate version
* HEAD → current branch
* Merge → combine branches
* Conflict → manual fix required

---

# 🎯 Conclusion

Branching is essential for:

* Safe development
* Collaboration
* Managing features without breaking main code
