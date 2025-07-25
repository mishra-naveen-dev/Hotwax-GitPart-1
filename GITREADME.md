
#  Git Commands Cheat Sheet

##  Configuration

```bash
# Set username
git config --global user.name "Your Name"

# Set email
git config --global user.email "youremail@example.com"

# Check current configuration
git config --list
```

---

## Repository Setupac

```bash
# Initialize a new repository
git init

# Clone an existing repository
git clone <repo-url>

# List remote repositories
git remote -v
```

---

## Basic Workflow

```bash
# Check current status
git status

# Add changes to staging area
git add <file>

# Commit staged changes
git commit -m "Commit message"

# Push changes to remote
git push

# Pull latest changes from remote
git pull

# Fetch changes from remote (without merging)
git fetch
```

---

## Branching

```bash
# Create a new branch
git branch <branch-name>

# Switch to an existing branch
git checkout <branch-name>

# Create and switch to a new branch
git checkout -b <branch-name>

# List all branches
git branch

# Merge another branch into the current branch
git merge <branch-name>

# Delete a branch
git branch -d <branch-name>

# Force delete a branch
git branch -D <branch-name>
```

---

##  Stashing

```bash
# Save changes to stash with a message
git stash save "Message"

# List all stashes
git stash list

# Apply the latest stash
git stash apply

# Apply a specific stash
git stash apply stash@{2}

# Delete the latest stash
git stash drop

# Delete a specific stash
git stash drop stash@{2}
```

---

## Tagging

```bash
# Create a lightweight tag
git tag <tag-name>

# List all tags
git tag

# Push tags to remote
git push --tags

# Delete a tag
git tag -d <tag-name>
```



