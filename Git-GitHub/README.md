# 🚀 Complete Git & GitHub Command Guide

This README is a complete cheat sheet of Git and GitHub commands with short explanations. Ideal for beginners and handy for experienced developers.

---

## 🔧 Git Configuration

```bash
git config --global user.name(Prasad) "Your Name"         # Set your Git username globally
git config --global user.email(prasadxy@12@gmail.com) "you@example.com"  # Set your Git email globally
git config --list                                 # View all current Git configs
```

## 🆕 Initialize a Repository
```bash
git init                                          # Initialize a new Git repo in current directory
```

## 📁 File Tracking & Commits
```bash
git status                                        # Check current changes and tracked files
git add file.txt                                  # Stage a specific file
git add .                                         # Stage all files
git commit -m "message"                           # Commit staged changes with a message
git commit --amend                                # Modify the last commit (message or files)
```

## 🌿 Branching and Merging
```bash
git branch                                        # List all local branches
git branch dev                                    # Create a new branch
git switch dev                                    # Switch to branch (Git 2.23+)
git checkout dev                                  # Switch to branch (older versions)
git merge dev                                     # Merge 'dev' into current branch
git branch -d dev                                 # Delete local branch
```

## 🔁 Undo Changes
```bash
git reset HEAD file.txt                           # Unstage a file
git restore file.txt                              # Discard changes to file
git checkout -- file.txt                          # Another way to discard changes
git revert <commit-id>                            # Create a new commit that undoes a commit
```

## 📜 Logs and Diffs
```bash
git log                                           # Show full commit history
git log --oneline --graph --all                   # Short and graphical log
git diff                                          # Show unstaged changes
git diff --staged                                 # Show staged but uncommitted changes
```

## 🌍 Connect to GitHub
```bash
git remote add origin https://github.com/Prasadk1618?tab=repositories   # Add remote repo
git remote -v                                             # Show remote connections
```

## ⬆️ Push and Pull
```bash
git push -u origin main                             # Push main to GitHub and set tracking
git push                                            # Push commits to tracked branch
git pull origin main                                # Pull updates from GitHub
git fetch                                           # Download changes without merging
```

## 🔄 Clone Repositories
```bash
git clone https://github.com/Prasadk1618?tab=repositories          # Clone GitHub repo to local machine
```

## 🏷️ Tagging Versions
```bash
git tag v1.0                                        # Create a lightweight tag
git tag                                             # List all tags
git push origin v1.0                                # Push specific tag to remote
```

## 🧪 Stash and Clean
```bash
git stash                                           # Save uncommitted changes temporarily
git stash apply                                     # Apply stashed changes
git stash list                                      # List stashes
git clean -fd                                       # Delete all untracked files and directories
```

##⚡ Git Shortcuts (Aliases)
```bash
git config --global alias.st status                # 'git st' for 'git status'
git config --global alias.co checkout              # 'git co' for 'git checkout'
git config --global alias.br branch                # 'git br' for 'git branch'
git config --global alias.cm "commit -m"           # 'git cm "msg"' to commit faster
```
## Made with ❤️ by Prasad — Cloud & DevOps Enthusiast ☁️🚀

---
