# Rebase Exercise

This exercise will guide you through the process of using Git rebase to integrate changes from one branch into another. Follow the steps below to complete the exercise.

## Steps to Complete the Exercise

1. **Create a Feature Branch**
   - Create a new feature branch named `feat/rebase-exercise` from the `main` branch:
   ```shell
   git checkout main
   git checkout -b feat/rebase-exercise
   ```

2. **Edit the `index.html` File**
   - Open the `index.html` file and make changes to the text in the body section.

3. **Make a Commit**
   - Stage your changes and commit them:
   ```shell
   git add index.html
   git commit -m "feat: update text in index.html"
   ```

4. **Switch to Main and Make Two Commits**
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

5. **Rebase Main into Your Feature Branch**
   - Switch back to your feature branch:
   ```shell
   git checkout feat/rebase-exercise
   ```
   - Rebase the `main` branch onto your feature branch:
   ```shell
   git rebase main
   ```

6. **Verify the Rebase**
   - After rebasing, your commits should now be on top of the `main` branch, and there should be no additional merge commits. You can check the commit history with:
   ```shell
   git log --oneline --graph --decorate
   ```

### Additional Resources

For more information on creating pull requests, refer to the [Creating Pull Requests Documentation](../docs/pull-requests.md).
