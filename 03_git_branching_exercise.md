
# 🧪 Git Hands-On Exercise: Working with Branches

## 🗂️ Objective:
Learn how to create, manage, and merge branches in Git by simulating a small project workflow.

---

## 📋 Prerequisites:
- Git installed on your computer.
- Basic understanding of command line and Git.
- A folder ready for use or create a new one.

---

## 🔨 Step-by-Step Activity

### ✅ Step 1: Initialize a Repository
```bash
mkdir git-branching-exercise
cd git-branching-exercise
git init
```

Create a file:
```bash
echo "Welcome to the main branch" > readme.txt
git add readme.txt
git commit -m "Initial commit on main branch"
```

---

### ✅ Step 2: Create a New Branch
Create a branch named `feature-hello`:
```bash
git branch feature-hello
```

Switch to it:
```bash
git checkout feature-hello
```

Edit the file:
```bash
echo "This is a new feature branch" >> readme.txt
git add readme.txt
git commit -m "Added feature message"
```

---

### ✅ Step 3: Merge the Branch into Main
Switch back to the main branch:
```bash
git checkout main
```

Merge the feature branch:
```bash
git merge feature-hello
```

---

### ✅ Step 4: Create and Delete Another Branch
Create a branch called `feature-goodbye`:
```bash
git checkout -b feature-goodbye
```

Edit the file:
```bash
echo "Goodbye from another branch!" >> readme.txt
git add readme.txt
git commit -m "Added goodbye message"
```

Switch to `main` and delete the branch after merging:
```bash
git checkout main
git merge feature-goodbye
git branch -d feature-goodbye
```

---

## 📌 Challenge:
1. Create another branch called `hotfix-typo`.
2. Edit `readme.txt` and fix a "typo" (add a line like `Fixed typo`).
3. Merge `hotfix-typo` back to main.
4. View the log of commits using:
   ```bash
   git log --oneline --graph
   ```
