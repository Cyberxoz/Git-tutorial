# Git-tutorial
It represent the full git tutorial , in which so many commands are present 
It is easy to learn
Absolutely — here is a **ready-to-paste Git tutorial section** for your `README.md`, written in simple language and organized from beginner to intermediate.

# Git & GitHub Tutorial

## 📌 What is Git?

**Git** is a distributed version control system used to track changes in source code and manage different versions of a project.

It allows developers to:

* Track changes in files
* Go back to previous versions
* Work on different features using branches
* Collaborate with other developers
* Maintain a complete history of a project

---

## 📌 Git vs GitHub

| Git                           | GitHub                                     |
| ----------------------------- | ------------------------------------------ |
| Git is a version control tool | GitHub is an online platform               |
| Runs on your computer         | Runs on the internet                       |
| Tracks changes in a project   | Stores and shares Git repositories         |
| Can work without internet     | Requires internet for online collaboration |
| Example: `git commit`         | Example: GitHub Repository                 |

> **Easy way to remember:** Git is the tool, while GitHub is an online platform that works with Git.

---

# 🚀 Installing Git

Download Git from the official Git website:

[https://git-scm.com/](https://git-scm.com/)

After installation, check whether Git is installed:

```bash
git --version
```

Example:

```text
git version 2.x.x
```

---

# ⚙️ Git Configuration

Set your username:

```bash
git config --global user.name "Your Name"
```

Set your email:

```bash
git config --global user.email "your@email.com"
```

Check your configuration:

```bash
git config --list
```

---

# 📁 Create a Git Repository

Go to your project folder:

```bash
cd my-project
```

Initialize Git:

```bash
git init
```

This creates a hidden `.git` folder that stores the Git history of your project.

---

# 🔍 Check Repository Status

Use:

```bash
git status
```

It shows:

* Modified files
* New/untracked files
* Staged files
* Current branch

---

# ➕ Git Add

Add a specific file:

```bash
git add filename
```

Example:

```bash
git add index.html
```

Add all changed files:

```bash
git add .
```

`git add` moves changes to the **Staging Area**.

---

# 💾 Git Commit

A commit saves the staged changes in Git's history.

```bash
git commit -m "Add homepage"
```

Example:

```bash
git commit -m "Add navbar"
```

### Good Commit Messages

```text
Add login page
Fix navbar bug
Update README
Add responsive design
Fix button alignment
```

---

# 📜 View Commit History

To see previous commits:

```bash
git log
```

Short version:

```bash
git log --oneline
```

---

# 🌐 Connect Local Repository to GitHub

First create a new repository on GitHub.

Then connect your local repository:

```bash
git remote add origin https://github.com/username/repository.git
```

Check the remote:

```bash
git remote -v
```

Rename the current branch to `main`:

```bash
git branch -M main
```

Push the project to GitHub:

```bash
git push -u origin main
```

After the first push, you can normally use:

```bash
git push
```

---

# 📤 Git Push

`git push` uploads your local commits to the remote repository such as GitHub.

```bash
git push
```

Typical workflow:

```bash
git add .
git commit -m "Update project"
git push
```

---

# 📥 Git Pull

`git pull` downloads the latest changes from the remote repository and updates your local project.

```bash
git pull
```

This is useful when working with a team or when changes were made directly on GitHub.

---

# 📥 Git Clone

If a project already exists on GitHub, you can download it using:

```bash
git clone https://github.com/username/repository.git
```

Then enter the project folder:

```bash
cd repository
```

---

# 🌿 Git Branches

A branch allows you to work on a feature without directly changing the `main` branch.

View branches:

```bash
git branch
```

Create a new branch:

```bash
git branch feature-login
```

Switch to the branch:

```bash
git switch feature-login
```

Create and switch to a branch in one command:

```bash
git switch -c feature-login
```

---

# 🔀 Git Merge

After completing your feature, you can merge it into the `main` branch.

Switch to main:

```bash
git switch main
```

Merge the feature branch:

```bash
git merge feature-login
```

---

# 🗑️ Delete a Branch

Delete a local branch:

```bash
git branch -d feature-login
```

Delete a remote branch:

```bash
git push origin --delete feature-login
```

---

# ↩️ Undo Changes

### Restore a modified file

```bash
git restore filename
```

Example:

```bash
git restore index.html
```

This restores the file to its previous committed state.

### Unstage a file

```bash
git restore --staged filename
```

This removes the file from the staging area without deleting your changes.

---

# 🚫 .gitignore

`.gitignore` tells Git which files and folders should **not** be tracked.

Example `.gitignore`:

```text
node_modules/
.env
dist/
*.log
```

For a Node.js project, `node_modules` is commonly added to `.gitignore`.

> Never upload passwords, API keys, private tokens, or other sensitive information to GitHub.

---

# 🔗 Git Remote

View remote repositories:

```bash
git remote -v
```

Add a remote:

```bash
git remote add origin https://github.com/username/repository.git
```

Change a remote URL:

```bash
git remote set-url origin https://github.com/username/repository.git
```

---

# 🧠 Git Areas

Git mainly works with three important areas:

```text
Working Directory
       ↓
    git add
       ↓
Staging Area
       ↓
  git commit
       ↓
Local Repository
       ↓
   git push
       ↓
GitHub / Remote Repository
```

### Working Directory

The files you are currently working on.

### Staging Area

Files selected to be included in the next commit.

### Local Repository

The Git history stored on your computer.

### Remote Repository

The repository stored online, such as on GitHub.

---

# 🔥 Complete Git Workflow

For everyday development, you will commonly use:

```bash
git status
git add .
git commit -m "Your message"
git push
```

If you are starting with an existing GitHub project:

```bash
git clone <repository-url>
cd <repository-name>
```

If you are creating a new local project:

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin <repository-url>
git branch -M main
git push -u origin main
```

---

# 📋 Common Git Commands Cheat Sheet

| Command                   | Purpose                               |
| ------------------------- | ------------------------------------- |
| `git init`                | Initialize a Git repository           |
| `git status`              | Check repository status               |
| `git add .`               | Stage all changes                     |
| `git add <file>`          | Stage a specific file                 |
| `git commit -m "message"` | Save changes to Git history           |
| `git log`                 | View commit history                   |
| `git clone <url>`         | Copy a remote repository              |
| `git push`                | Upload commits to remote repository   |
| `git pull`                | Download and integrate remote changes |
| `git branch`              | View branches                         |
| `git switch <branch>`     | Switch branches                       |
| `git switch -c <branch>`  | Create and switch to a branch         |
| `git merge <branch>`      | Merge a branch                        |
| `git restore <file>`      | Restore file changes                  |
| `git remote -v`           | View remote repositories              |

---

# ⭐ Recommended Git Workflow

```text
1. Create or clone a project
          ↓
2. Make changes
          ↓
3. git status
          ↓
4. git add .
          ↓
5. git commit -m "Meaningful message"
          ↓
6. git push
          ↓
7. Changes appear on GitHub
```

### Example

```bash
git status
git add .
git commit -m "Add contact page"
git push
```

> **Remember:**
> `git add` → Select changes
> `git commit` → Save changes
> `git push` → Upload changes to GitHub
