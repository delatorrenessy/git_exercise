````markdown
# 🧠 Git Team Collaboration Practice

## 🔧 Scenario
Alice and Bob are teammates working on the same project.

- Alice wants to build something new, so she works on a **feature branch**.  
- Bob makes updates to the **main branch**.  
- They need to **share their work and combine it safely** using Git.

---

## 🎯 What You’ll Learn

- How to make and switch branches  
- How to save and share your work (commit & push)  
- How to get your teammate’s updates (pull)  
- How to combine work and fix problems (merge & resolve conflicts)

---

## 👨‍🏫 Teacher Setup

1. Make a GitHub repo called **`collab-demo`**
2. Add a file like `README.md`
3. Invite Alice and Bob as collaborators

---

## 👩‍💻 Alice’s Instructions – Work on a Feature

### Step 1: Get the project on her computer

```bash
git clone https://github.com/your-org/collab-demo.git
cd collab-demo
````

### Step 2: Start her own branch

```bash
git checkout -b feature-alice
```

### Step 3: Make a change

```bash
echo "Alice was here." >> README.md
```

### Step 4: Save the change

```bash
git add README.md
git commit -m "Added a line by Alice"
```

### Step 5: Share her branch to GitHub

```bash
git push origin feature-alice
```

---

## 👨‍💻 Bob’s Instructions – Update the Main Branch

### Step 1: Get the project on his computer

```bash
git clone https://github.com/your-org/collab-demo.git
cd collab-demo
```

### Step 2: Stay on main branch and make a change

```bash
echo "Bob updated the main branch." >> README.md
```

### Step 3: Save the change

```bash
git add README.md
git commit -m "Bob's update to main"
```

### Step 4: Share the change to GitHub

```bash
git push origin main
```

---

## 🔄 Alice Brings Bob’s Updates into Her Branch

### Step 1: Go back to her branch

```bash
git checkout feature-alice
```

### Step 2: Get Bob’s latest changes

```bash
git pull origin main
```

### Step 3: If there’s a problem (merge conflict), fix it

```bash
# After fixing:
git add .
git commit -m "Merged main into feature-alice"
```

### Step 4: Share her updated branch

```bash
git push origin feature-alice
```

---

✅ **Done!** Alice and Bob have worked on the same project, shared their changes, and combined their work using Git.
