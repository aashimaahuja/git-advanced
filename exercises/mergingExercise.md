# Merging Exercise

This exercise will guide you through the process of merging branches in Git. Follow the steps below carefully to complete the exercise.

## Part 1: Merging a Feature Branch

1. **Create a Feature Branch**
   - Create a new feature branch named `feat/merge-exercise` from the `main` branch:
   ```shell
   git checkout main
   git checkout -b feat/merge-exercise
   ```

2. **Edit the `index.html` File**
   - Open the `index.html` file and change some text in the body section.

3. **Make a Commit**
   - Stage your changes and commit them:
   ```shell
   git add index.html
   git commit -m "feat: update text in index.html"
   ```

4. **Switch to main and Make Two Commits**
   - Go back to the `main` branch:
   ```shell
   git checkout main
   ```
   - Make two separate commits with any changes you like. For example:
   ```shell
   echo "First change in main" >> somefile.txt
   git add somefile.txt
   git commit -m "chore: add first change in main"

   echo "Second change in main" >> anotherfile.txt
   git add anotherfile.txt
   git commit -m "chore: add second change in main"
   ```

5. **Merge main into Your Feature Branch**
   - Switch back to your feature branch:
   ```shell
   git checkout feat/merge-exercise
   ```
   - Merge the `main` branch into your feature branch:
   ```shell
   git merge main
   ```

6. **Verify the Merge**
   - After merging, you should see the commits from `main` along with a new merge commit in your feature branch. You can check the commit history using:
   ```shell
   git log --oneline --graph --decorate
   ```

## Part 2: (Optional)

1. **Make Additional Commits**
   - In your feature branch, make one more commit and in the `main` branch, make two more commits.

2. **Merge main with Squash**
   - Merge the `main` branch into your feature branch using the squash option:
   ```shell
   git merge --squash main
   ```
   - Name your commit appropriately:
   ```shell
   git commit -m "feat: squash merge main changes into feature branch"
   ```

3. **Check for Merge Commits**
   - After the squash merge, there should be no merge commit created. Verify the commit history again using:
   ```shell
   git log --oneline --graph --decorate
   ```

### Additional Resources

For more information on rebasing, refer to the [Rebase Documentation](../docs/rebase.md).
