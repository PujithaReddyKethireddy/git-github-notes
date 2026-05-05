# 🌿 Branching & Merging in Git

This section provides a **detailed explanation of branching, merging, and conflict handling in Git**, based on:

* CS50 Web Programming (Harvard)
* Git Learning
* Real-world development practices

Branching is one of the **most powerful features of Git**, enabling safe and efficient development.

---

# 📌 1. What is a Branch?

A **branch** is an independent line of development in Git.

When you create a branch, Git creates a new pointer to the current commit. From that point onward, changes in that branch do not affect other branches.

👉 This allows you to:

* Work on features independently
* Fix bugs safely
* Experiment without breaking the main code

📖 From CS50:
Branching allows development **without affecting the main codebase**, and changes can be merged later.

---

# 📌 2. Why Branching is Important

Without branching:

* All development happens in one place ❌
* Bugs can break the entire project ❌

With branching:

* Features are isolated ✔
* Main branch stays stable ✔
* Multiple developers can work simultaneously ✔

👉 This is the foundation of **team-based development**.

---

# 📌 3. Creating a Branch

```bash
git branch <branch_name>
```

This creates a new branch but does not switch to it.

---

# 📌 4. Switching Branches

### Traditional command:

```bash
git checkout <branch_name>
```

### ✅ Modern command (Recommended):

```bash
git switch <branch_name>
```

👉 `git switch` is clearer and safer because:

* It is only used for switching branches
* It avoids confusion with file operations

---

# 📌 5. Create + Switch (Best Practice)

### Traditional:

```bash
git checkout -b <branch_name>
```

### ✅ Modern:

```bash
git switch -c <branch_name>
```

👉 This is the most commonly used workflow in real projects.

---

# 📌 6. Check Current Branch

```bash
git branch
```

👉 Output example:

```text
* main
  feature-login
```

* `*` indicates the current branch
* This is a key visual indicator

---

# 📌 7. HEAD Concept (VERY IMPORTANT)

**HEAD** is a pointer that indicates your current working branch.

* By default → HEAD → main
* When switching branches → HEAD moves

👉 All commits are added where HEAD points.

---

# 📌 8. Visualizing Branch Structure

```text
main:     A --- B --- C
                   \
feature:            D --- E
```

After merge:

```text
main:     A --- B --- C -------- F
                   \          /
feature:            D --- E
```

👉 This shows how branches diverge and rejoin.

---

# 📌 9. Merging Branches

```bash
git switch main
git merge <branch_name>
```

Merging combines changes from one branch into another.

---

## 🔹 Types of Merge

### 1. Fast-Forward Merge

* Happens when main has no new commits
* Git simply moves the pointer forward

👉 No merge commit created

---

### 2. Three-Way Merge

* Happens when both branches have changes
* Git creates a new **merge commit**

👉 This is the most common scenario

---

# 📌 10. Deleting a Branch

```bash
git branch -d <branch_name>
```

👉 Deletes a branch safely

⚠️ Important:

* Git will prevent deletion if the branch is not merged

### Force delete:

```bash
git branch -D <branch_name>
```

👉 Use carefully — this deletes unmerged work

---

# 📌 11. Merge Conflicts (CRITICAL)

A **merge conflict** occurs when:

* Two branches modify the same part of a file differently

---

## 🔹 Conflict Example

```text
<<<<<<< HEAD
b = 2    # current branch
=======
b = 3    # incoming branch
>>>>>>> feature-login
```

👉 You must manually decide:

* Keep one version
* Or combine both

---

# 📌 12. Resolving Conflicts

Steps:

1. Open file
2. Remove conflict markers
3. Fix code
4. Save

Then:

```bash
git add <file>
git commit -m "Resolved conflict"
```

---

# 📌 13. Branch Workflow (REAL DEVELOPMENT)

```bash
git switch -c feature-login

# make changes

git add .
git commit -m "Added feature"

git switch main
git pull
git merge feature-login
```

👉 This is the standard industry workflow.

---

# 📌 14. Key Concepts Summary

* Branch → Independent version
* HEAD → Current branch pointer
* Merge → Combine changes
* Conflict → Manual resolution required

---

# 🎯 Conclusion

Branching enables:

* Safe feature development
* Parallel work
* Stable main codebase

👉 It is essential for:

* Team collaboration
* Real-world software development
* Scalable projects
