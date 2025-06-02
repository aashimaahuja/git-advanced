# Git Command Cheatsheet

## Basic Commands

### Check Status & Info
```shell
# Check git version
git --version

# Check status
git status
git status -s  # Short status

# View history
git log
git log --oneline
git log --stat
git log --graph
```

### Repository Setup
```shell
# Initialize repository
git init

# Add files
git add <file_name>
git add .  # Add all files
git add --all  # Add all files including deleted ones

# Commit changes
git commit -m "<message>"
git commit -am "<message>"  # Add and commit tracked files
git commit --amend -m "<message>"  # Edit last commit message
git commit --amend --no-edit  # Add to last commit without editing message
```

## Configuration
```shell
# Set user info
git config --global user.name "<name>"
git config --global user.email "<email>"

# View config
git config --list
git config --list --show-origin

# Multiple configs
[includeIf "gitdir:~/work/"]
    path = ~/.gitconfig-work
[includeIf "gitdir:~/personal/"]
    path = ~/.gitconfig-personal
```

## Remote Operations
```shell
# Add remote
git remote add <remote_name> <remote_url>

# View remotes
git remote -v

# Rename remote
git remote rename <old_name> <new_name>

# Clone repository
git clone <remote_url>

# Push changes
git push <remote> <branch>
git push -u <remote> <branch>  # Set upstream
git push --force  # Force push (use with caution)

# Pull changes
git pull <remote> <branch>
git pull --rebase  # Pull with rebase

# Fetch changes
git fetch <remote>
```

## Branch Operations
```shell
# List branches
git branch
git branch -a  # List all branches including remote

# Create branch
git branch <branch_name>
git checkout -b <branch_name>  # Create and switch
git switch -c <branch_name>    # Create and switch (new syntax)

# Switch branches
git checkout <branch_name>
git switch <branch_name>

# Delete branch
git branch -d <branch_name>
git branch -D <branch_name>  # Force delete
```

## Merging & Rebasing
```shell
# Merge
git merge <branch_name>
git merge --squash <branch_name>

# Rebase
git rebase <branch_name>
git rebase -i HEAD~<n>  # Interactive rebase last n commits

# Cherry-pick
git cherry-pick <commit_hash>
```

## Undoing Changes
```shell
# Discard changes in working directory
git restore <file_name>
git checkout <file_name>  # Old syntax

# Unstage changes
git restore --staged <file_name>
git reset <file_name>

# Reset commits
git reset --hard HEAD
git reset --hard <commit_hash>
git reset --soft <commit_hash>

# Revert commit
git revert <commit_hash>

# View reflog (recovery)
git reflog
```

## Tags
```shell
# List tags
git tag

# Create tag
git tag -a <tag_name> -m '<message>'
git tag <tag_name>  # Lightweight tag

# Delete tag
git tag --delete <tag_name>

# Show tag info
git show <tag_name>
```

## Stash Operations
```shell
# Save changes to stash
git stash push
git stash push -u -k  # Include untracked files

# Apply stashed changes
git stash pop
git stash apply

# List stashes
git stash list
```

## Diff & Status
```shell
# View differences
git diff
git diff --staged
git diff <branch1> <branch2>
git diff master origin/master

# Show commit details
git show <commit_hash>
```

## Best Practices

### Commit Messages
- Use conventional commit messages: `<type>[optional scope]: <description>`
- Types: feat, fix, docs, style, refactor, test, chore
- Write in present tense
- Keep messages clear and concise
- Example: `feat(auth): add user authentication system`

### Branch Naming
- Use descriptive names with type prefixes
- Format: `<type>/<description>`
- Examples:
  - `feature/user-auth`
  - `bugfix/login-error`
  - `hotfix/security-patch`

### Important Notes
- Don't rebase commits that have been pushed to shared repositories
- Always pull before pushing to avoid conflicts
- Use `.gitignore` for files that shouldn't be tracked
- Review changes before committing
