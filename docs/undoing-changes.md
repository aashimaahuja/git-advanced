# Undoing Changes in Git

Managing changes effectively is crucial in Git, especially when mistakes happen. This guide covers various methods to undo changes, unstage files, and revert commits.

## 1. Undo Changes in a File

If you've made changes to a file and want to discard them, you can use:

```shell
git checkout <file_name>
```

or 

```shell
git restore <file_name>
```

### Note:
- **Caution**: Using these commands will permanently delete any uncommitted changes in the specified file.

## 2. Unstage Staged Changes

If you've added changes to the staging area but want to unstage them, you can use:

```shell
git restore --staged <file_name>
```

or 

```shell
git reset <file_name>
```

To unstage all files:

```shell
git reset .
```

### Note:
- These commands will only remove the files from the staging area; your changes will still be present in your working directory.

## 3. Undo Commits

### Using `git reset`

The `git reset` command allows you to remove commits or reset a branch to a specific commit. There are three types of resets:

- **Hard Reset**: Removes commits and does not keep changes in the working directory.
  
  ```shell
  git reset <commit_hash> --hard
  ```

- **Soft Reset**: Removes commits but keeps changes in the working directory.
  
  ```shell
  git reset <commit_hash>
  ```

### Visual Representation

<img src="../images/reset-commit-1.png" width="50%" height="50%" />
<img src="../images/reset-commit-2.png" width="50%" height="50%" />

### Important Consideration

**Issue with Reset**: 
Using `git reset` can lead to losing shared history if you reset commits that others have based their work on. Always communicate with your team before performing a reset.

### Using `git revert`

The `git revert` command undoes commits by creating a new commit that reverses the changes made by the specified commit. This method is safe for published commits since it does not alter the project history.

```shell
git revert <commit_hash>
```

### Visual Representation

<img src="../images/undo-commits-2.png" width="500" height="300" />

### Advantages of `git revert`

- **Safety**: It is a safer option to undo a commit, especially if the commit has already been pushed to a remote repository. It maintains the integrity of the commit history.

## Additional Resources

For more information on branching and managing your repository, refer to the [Branches](../docs/branches.md) document.
