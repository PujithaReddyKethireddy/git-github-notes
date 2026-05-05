# 🚀 Git & GitHub – Complete Guide (CS50 + W3Schools + Practice)

This repository contains my **complete understanding of Git & GitHub**, built from:

* 📘 CS50 Web Programming (Harvard)
* 🌐 W3Schools Git Tutorial
* 💻 Hands-on terminal practice

---

# 📌 1. What is Git?

Git is a **Version Control System (VCS)** used to:

* Track changes in code
* Save **snapshots (commits)** of projects
* Collaborate with multiple developers
* Restore previous versions anytime

👉 Instead of saving multiple files manually:

```
file_v1 → file_v2 → file_final
```

Git stores:
👉 **Snapshots of your project over time**

📖 From CS50:
Git allows us to **track changes, revert versions, and collaborate efficiently** 

---

# 🌐 2. What is GitHub?

GitHub is a **cloud platform** to store Git repositories.

👉 It allows:

* Remote storage
* Collaboration
* Code sharing
* Version syncing

📖 From CS50:
A repository is a **project folder stored locally or remotely** 

---

# ⚙️ 3. Git Workflow (CORE)

```
Working Directory → Staging Area → Local Repository → Remote Repository
```

### Example:

```bash
git add .
git commit -m "Added feature"
git push origin main
```

---

# 🔄 4. How Git Works (REAL UNDERSTANDING)

Git follows 3 main steps:

| Step   | Command    | Meaning          |
| ------ | ---------- | ---------------- |
| Add    | git add    | Select files     |
| Commit | git commit | Save snapshot    |
| Push   | git push   | Upload to GitHub |

📖 From CS50:

* `git add` → select files
* `git commit` → save snapshot
* `git push` → upload changes 

---

# 🧾 5. Important Git Commands

## 🔹 Clone Repository

```bash
git clone <repo-url>
```

👉 Downloads project from GitHub

---

## 🔹 Check Status

```bash
git status
```

👉 Shows current changes

---

## 🔹 Add Files

```bash
git add file.txt
git add .
```

---

## 🔹 Commit Changes

```bash
git commit -m "Added login feature"
```

👉 Saves snapshot

---

## 🔹 Push Changes

```bash
git push origin main
```

👉 Uploads to GitHub

---

## 🔹 Pull Changes

```bash
git pull origin main
```

👉 Downloads latest code

📖 From CS50:

* Push → upload changes
* Pull → download updates from others 

---

# 🌿 6. Branching (VERY IMPORTANT)

Branch = Separate version of code

👉 Used to:

* Develop features
* Fix bugs safely

📖 From CS50:
Branching lets us **work on features without affecting main code** 

---

## 🔹 Create Branch

```bash
git checkout -b feature-login
```

## 🔹 Switch Branch

```bash
git checkout main
```

---

# 🔀 7. Merging

```bash
git checkout main
git merge feature-login
```

👉 Combines feature into main

---

# ⚠️ 8. Merge Conflict (IMPORTANT)

Occurs when:
👉 Same line edited differently

Example:

```bash
<<<<<<< HEAD
int a = 10;
=======
int a = 20;
>>>>>>> branch
```

📖 From CS50:
You must manually **choose or combine changes** 

---

# 🔁 9. Push vs Pull (INTERVIEW QUESTION)

| Command  | Meaning            |
| -------- | ------------------ |
| git push | Upload changes     |
| git pull | Get latest changes |

---

# 🔍 10. Git Log

```bash
git log
```

👉 Shows:

* Commit history
* Author
* Date
* Changes

---

# 🔄 11. Undo Changes

## Reset to previous commit

```bash
git reset --hard <commit-id>
```

## Reset to GitHub version

```bash
git reset --hard origin/main
```

📖 From CS50:
Git allows reverting to **previous snapshots easily** 

---

# 🌍 12. GitHub Features

## 🔹 Fork

👉 Copy someone else's repo

## 🔹 Pull Request

👉 Request to merge your changes

## 🔹 GitHub Pages

👉 Host websites for free

---

# 🔍 13. Real Workflow (PROJECT)

```bash
git clone <repo>
cd repo

git checkout -b feature-auth

# make changes

git add .
git commit -m "Added authentication"

git push origin feature-auth

git checkout main
git merge feature-auth
```

---

# 🧠 14. Best Practices

✅ Write clear commit messages
✅ Pull before push
✅ Use branches
✅ Keep commits small
✅ Avoid conflicts

---

# 🎯 15. Why Git is Important

* Industry standard tool
* Used in all software companies
* Essential for teamwork
* Enables large project management

---

# 📁 16. Repository Structure

```
basics/
branching/
practice/
```

---

# 💼 Author

**Pujitha Reddy**

---

⭐ Star this repo if you find it useful!
