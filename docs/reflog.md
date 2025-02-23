# Reflog

The reflog is a powerful tool in Git that allows you to recover lost commits and deleted branches. This document outlines common scenarios for using reflog effectively.

## Recover Lost Commits

<details>
<summary><strong>Scenario: You Made a Commit, Did a Hard Reset, and Lost That Commit</strong></summary>

If you’ve realized that you’ve lost a commit after performing a hard reset and are in a panic, follow these steps:

1. First, check your reflog to see the history of your commits:

   ```shell
   git reflog
   ```

2. Look for the commit hash that corresponds to the state you want to recover (the one just before the reset).

3. You can recover the lost commit by either:

   - **Option A:** Resetting to the specific commit:

     ```shell
     git reset --hard <hash>
     ```

   - **Option B:** Creating a new branch from that commit:

     ```shell
     git branch <branch_name> <hash>
     ```

</details>

## Recover Accidentally Deleted Branch

<details>
<summary><strong>Scenario: You Accidentally Deleted a Feature Branch</strong></summary>

If you’ve deleted a feature branch and need to recover it, follow these steps:

1. Check your reflog to find the commit associated with the deleted branch:

   ```shell
   git reflog
   ```

2. Locate the commit hash related to the deleted branch.

3. Restore the branch using:

   ```shell
   git branch <branch_name> <hash>
   ```

4. Verify that the branch has been restored by listing all branches:

   ```shell
   git branch
   ```

</details>

---

### Additional Notes

- The reflog stores a history of your references, making it easier to recover from mistakes. It's important to familiarize yourself with these commands to effectively manage your Git repository.
- Regularly check your reflog, especially before performing destructive actions like `reset --hard`.

Feel free to reach out if you have any questions or need further assistance!
