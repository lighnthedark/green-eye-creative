# Git Commands Cheat Sheet
### Spencer Green — Lee's Legacy Dev Notes

---
=
## Every Day Commands
```bash
git add .                        # Stage all changed files
git commit -m "message"          # Save a snapshot with a message
git push                         # Send commits to GitHub
git status                       # See what's changed/staged/untracked
git log --oneline                # See commit history in short form
git log --oneline -5             # See last 5 commits only
```

---

## Fixing Mistakes
```bash
git checkout <hash> -- path/file   # Restore a file from a specific commit
git checkout HEAD -- path/file     # Restore a file to its last committed state
git revert <hash>                  # Undo a commit safely (keeps history)
git reset --hard HEAD              # Nuclear option — wipe all uncommitted changes
```

---

## Investigating
```bash
git show HEAD:path/to/file         # See what a file looks like in latest commit
git ls-files path/to/file          # Check if a file is tracked by git
git diff                           # See what changed since last commit
git diff HEAD~1                    # Compare with one commit ago
git log --oneline --all            # See ALL commits including other branches
```

---

## Branches
```bash
git branch                         # List all branches
git branch new-feature             # Create a new branch
git checkout new-feature           # Switch to a branch
git checkout -b new-feature        # Create AND switch in one command
git merge new-feature              # Merge a branch into current branch
```

---

## Remote / GitHub
```bash
git remote -v                      # See where you're pushing to
git pull                           # Pull latest changes from GitHub
git fetch                          # Check for changes without merging
git clone <url>                    # Copy a repo to your machine
```

---

## Force / Emergency
```bash
git add -f filename                # Force add a file (even if ignored)
git rm --cached filename           # Stop tracking a file without deleting it
git stash                          # Temporarily save uncommitted changes
git stash pop                      # Bring stashed changes back
```

---

## Interview Answers

**"Walk me through your git workflow"**
> I use feature branches for new work. I commit small and often with clear messages. 
> I push to GitHub regularly so nothing is lost. I use git log and git diff to 
> review before merging. I've used git checkout to restore accidentally deleted files.

**"What's the difference between git fetch and git pull?"**
> Fetch downloads changes from remote but doesn't apply them. 
> Pull downloads AND merges them into your current branch.

**"What's a merge conflict and how do you resolve it?"**
> When two branches changed the same line of code differently. 
> Git marks the conflict in the file. You manually edit it to keep 
> the right version, then git add and commit to resolve it.

**"What's git revert vs git reset?"**
> Revert creates a new commit that undoes a previous one — safe for shared repos.
> Reset moves the branch pointer back — rewrites history, dangerous on shared branches.

---

*Built during Lee's Legacy development — March 2026*
*"Even the biggest tree started from the smallest seed." 🌳*
