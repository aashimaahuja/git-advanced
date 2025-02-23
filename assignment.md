# Undo Mistakes in Git

This document outlines common scenarios for undoing mistakes in Git. Each scenario includes the necessary commands to rectify the issue.

<div style="display:flex; flex-direction:column; gap:16px">

<details>
<summary><strong>Discard Uncommitted Changes in a File</strong></summary>
  
To discard changes made to a specific file, use:

```shell
git restore <filename>
```
</details>

<details>
<summary><strong>Restore a Deleted File</strong></summary>
  
If you accidentally deleted a file, you can restore it with:

```shell
git restore <filename>
```
</details>

<details>
<summary><strong>Fix a Typo in Your Commit Message</strong></summary>
  
To amend the last commit message, run:

```shell
git commit --amend -m "<new_message>"
```

> **Note:** Amending a commit changes its hash, creating a new commit. Avoid amending if the commit has already been pushed to the remote repository.
</details>

<details>
<summary><strong>Add a Forgotten File to the Last Commit</strong></summary>

If you forgot to include a file in your last commit, do the following:

```shell
git add <forgotten_filename>
git commit --amend --no-edit
```
</details>

<details>
<summary><strong>Discard All Changes and Revert to the Previous State</strong></summary>

If your code refactoring didn't work and you want to discard all changes:

```shell
git reset --hard HEAD
```
</details>

<details>
<summary><strong>Remove Recent Commits</strong></summary>

To remove recent commits from your repository:

![Removing Commits](./images/image-17.png)

Run:

```shell
git reset --hard <commit_hash>
```
</details>

<details>
<summary><strong>Move a Commit from Main to a Feature Branch</strong></summary>

If you accidentally committed to the main branch instead of the feature branch, follow these steps:

**Move Commit to Feature Branch:**
```shell
git checkout <feature_branch>
git cherry-pick <commit_hash>
```

**Remove Commit from Main:**
```shell
git reset --hard HEAD~1
```
</details>

<details>
<summary><strong>Recover a Lost Commit After a Hard Reset</strong></summary>

If you performed a hard reset and lost a commit, don't panic! Use:

```shell
git reflog
```

Find the hash of the commit just before the reset and run either:

```shell
git reset --hard <hash>
```
or

```shell
git branch <branch_name> <hash>
```
</details>

<details>
<summary><strong>Recover a Deleted Feature Branch</strong></summary>

If you accidentally deleted a feature branch, you can recover it with:

```shell
git reflog
```

Find the commit associated with the feature branch and run:

```shell
git branch <branch_name> <hash>
```
</details>

</div>

## Additional Resources

For more tips and tricks, check out the [Bonus Section](./docs/aliases.md).
