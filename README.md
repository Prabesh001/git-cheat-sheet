
# 🧰 Git Essentials – Cheat Sheet

A complete reference of the most commonly used Git commands for initializing, managing, and collaborating in Git repositories.

---

## 🔧 Git Configuration

Set up your identity and default settings:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global init.defaultBranch main
```

---

## 📁 Starting a Project

```bash
git init                         # Create a new Git repository
git clone <repo-url>             # Clone an existing repo from GitHub or other
```

---

## 💾 Saving Changes

```bash
git status                       # Show changed files
git add <file>                   # Stage a specific file
git add .                        # Stage all changes
git commit -m "message"          # Commit staged changes
git commit -am "message"         # Add & commit tracked files (skip 'add')
```

---

## 🔍 Viewing History

```bash
git log                          # Full commit history
git log --oneline                # Condensed log
git diff                         # Show unstaged changes
git diff --staged                # Show staged changes
```

---

## 🌿 Branching

```bash
git branch                       # List branches
git branch <name>                # Create a new branch
git checkout <name>              # Switch to branch
git checkout -b <name>           # Create and switch to new branch
git merge <name>                 # Merge another branch into current
git branch -d <name>             # Delete a branch
```

---

## 🔄 Remote Repositories

```bash
git remote -v                    # List remotes
git remote add origin <url>      # Add a remote
git push -u origin main          # Push branch and set upstream
git push                         # Push changes
git pull                         # Fetch and merge from remote
git fetch                        # Fetch from remote (no merge)
```

---

## 🧹 Undoing Changes

```bash
git restore <file>              # Discard unstaged changes to a file
git restore --staged <file>     # Unstage a file
git reset --hard                # Reset all changes to last commit
git reset HEAD~1                # Undo last commit (keep changes unstaged)
```

---

## 🗑️ **Removing Git from a Project**

### **Method 1: Using Terminal (Unix-based systems or Git Bash)**

```bash
rm -rf .git                     # Remove all Git tracking and history (for Unix systems or Git Bash)
```

### **Method 2: Forceful Measures for Windows PowerShell**

```powershell
Remove-Item -Recurse -Force .git   # Force delete .git folder in PowerShell (Windows)
```

- **Explanation**:
    - `-Recurse`: Deletes all contents inside `.git`
    - `-Force`: Forces deletion of hidden and read-only files

### **Troubleshooting Steps if the above doesn't work:**

1. **Make sure you're inside the correct project directory**:
    ```bash
    ls -a
    ```
    Look for the `.git` folder.

2. **On Windows**: If you're using PowerShell, make sure no other processes (e.g., Git GUI, VS Code) are using `.git`. You can try closing any Git-based GUI or IDE before running the command.

3. **Manually Delete the `.git` Folder**:  
    If the terminal command isn't working, go to your **File Explorer** and enable "Show Hidden Files." Delete the `.git` folder manually.

---

## 📌 Miscellaneous

```bash
git stash                       # Temporarily save changes
git stash pop                   # Re-apply stashed changes
git show <commit-id>            # Show details of a specific commit
```

---

## 🧰 Helpful Aliases (Optional)

```bash
git config --global alias.s status
git config --global alias.c "commit -m"
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.l "log --oneline --graph --all"
```

---

## 📚 Resources

- [Git Official Docs](https://git-scm.com/doc)
- [GitHub Docs](https://docs.github.com/)
- [Learn Git Branching (Interactive)](https://learngitbranching.js.org/)

---
