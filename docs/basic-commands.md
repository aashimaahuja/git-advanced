## Git Basic Commands

This document provides a quick reference to essential Git commands for version control.

### 1. Check Status

To view the current status of your repository, including staged, unstaged, and untracked files:

```shell
git status
```

### 2. Add Files

To stage specific files for commit:

```shell
git add fileOne.txt fileTwo.txt
```

To stage all changes in the current directory:

```shell
git add .
```

### 3. Unstage Files

To remove a file from the staging area:

```shell
git reset <file_name>
```

### 4. Create a Commit

To create a commit with a message:

```shell
git commit -m "<commit_message>"
```

To stage and commit changes in one command (only for tracked files):

```shell
git commit -am "<commit_message>"
```

### 5. Check Commit History

To view the commit history:

```shell
git log
```

For a more concise view of the commit history:

```shell
git log --oneline
```

### 6. Fetch Remote Changes

To fetch updates from a remote repository without merging:

```shell
git fetch <remote_name>
```

### 7. Calculate Diff

To compare differences between your local branch and the remote branch:

```shell
git diff master origin/master
```

### 8. Pull Changes

To pull changes from a remote branch and merge them into your current branch:

```shell
git pull <remote> <branch>
```

### 9. Push Changes

To push your local commits to a remote repository:

```shell
git push <remote> <branch>
```

To forcefully push changes (use with caution):

```shell
git push --force
```

### 10. Create a New Branch

To create a new branch:

```shell
git branch <branch_name>
```

### 11. Checkout Command

#### Switch Branches

To switch to a different branch:

```shell
git checkout <branch_name>
```

#### Undo Changes in a File

To discard changes in a specific file:

```shell
git checkout <file_name>
```

#### Moving to a Commit or Tag

To switch to a specific commit or tag:

```shell
git checkout <commit_hash>
```

*Note: When you checkout to a commit, you enter a detached HEAD state, meaning the changes do NOT belong to any branch.*

![Git Checkout](../images/image-11.png)

### 12. Stashing Changes (Optional)

Temporarily store changes for later use. 

#### Stash Changes

To stash your changes:

```shell
git stash push
```

To stash all changes, including untracked files:

```shell
git stash push -u -k
```

#### Apply Stash

To apply the most recent stash:

```shell
git stash pop
```

---

### Additional Resources

- [Commits](commits.md)
