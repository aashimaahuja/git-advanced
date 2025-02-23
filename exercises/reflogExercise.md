# Reflog Exercise

This exercise will guide you through using Git's reflog to recover lost commits after a hard reset. Follow the steps below carefully.

## Objectives

1. **Delete the last two commits in your main branch using `reset --hard`.**
2. **Recover the last two commits using reflog.**

## Instructions

### Step 1: Delete the Last Two Commits

1. Open your terminal and navigate to your Git repository.
2. Make sure you are on the `main` branch:

   ```shell
   git checkout main
   ```

3. To delete the last two commits, run:

   ```shell
   git reset --hard HEAD~2
   ```

   **Note:** This command will permanently delete the last two commits and all uncommitted changes in your working directory. Ensure you really want to do this!

### Step 2: Recover the Last Two Commits

1. After deleting the commits, view your reflog to find the commit hashes:

   ```shell
   git reflog
   ```

   This command will display a list of actions you've performed in your repository, along with their corresponding commit hashes.

2. Identify the hashes of the last two commits you deleted. They should be listed at the top of the reflog output.

3. To recover the last two commits, you can either:

   - **Option A:** Reset to the commit before the reset:

     ```shell
     git reset --hard <commit_hash>
     ```

   - **Option B:** Create a new branch from the commit:

     ```shell
     git branch recovered-branch <commit_hash>
     ```

4. Verify that your commits have been successfully recovered by checking your commit history:

   ```shell
   git log --oneline
   ```

### Additional Resources

- [Git Aliases](../docs/aliases.md)

---

By completing this exercise, you should now be familiar with using `git reflog` to recover lost commits after a hard reset. Practice this technique to enhance your Git skills!
