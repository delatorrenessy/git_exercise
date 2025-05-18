# 👨‍💻 Git Team Collaboration Exercise

## 🔧 Scenario:
Alice and Bob are working on the same project.  
- **Alice** creates a new branch to add a feature.  
- **Bob** updates the `main` branch with changes.  
They must use `git pull`, `git push`, and `git merge` to collaborate properly.

---

## 🧩 Objective:
Practice collaborative Git operations:
- Creating and switching branches
- Committing and pushing changes
- Pulling latest updates
- Merging branches and resolving merge conflicts

---

## 🪜 Step-by-Step Instructions

### 🧑‍🤝‍🧑 Instructor Setup
1. Create a GitHub repo: `collab-demo`
2. Add initial content (e.g., `README.md`)
3. Invite Alice and Bob as collaborators

---

### 👩‍💻 Alice’s Tasks – Feature Branch Workflow

```bash
# 1. Clone the repository
git clone https://github.com/your-org/collab-demo.git
cd collab-demo

# 2. Create and switch to a new branch
git checkout -b feature-alice

# 3. Make changes
echo "Alice was here." >> README.md

# 4. Commit the changes
git add README.md
git commit -m "Added a line by Alice"

# 5. Push the branch to GitHub
git push origin feature-alice

---

### 👩‍💻 Bob’s Tasks – Update Main Branch

```bash
# 1. Clone the repository
git clone https://github.com/your-org/collab-demo.git
cd collab-demo

# 2. Stay on main and make updates
echo "Bob updated the main branch." >> README.md

# 3. Commit the changes
git add README.md
git commit -m "Bob's update to main"

# 4. Push to main branch
git push origin main

---

### 👩‍💻 Alice Merges Main into Her Branch

```bash
# 1. Switch to her feature branch
git checkout feature-alice

# 2. Pull latest updates from main
git pull origin main

# 3. If needed, resolve merge conflicts, then:
git add .
git commit -m "Merged main into feature-alice"

# 4. Push the updated feature branch
git push origin feature-alice

