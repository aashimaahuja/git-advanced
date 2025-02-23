# Pull Request Exercise

## Part 1: Bugfix Branch

In your **git-workshop** project, follow these steps to create a bugfix branch and submit a pull request:

1. **Create a Bugfix Branch**
   - From the `main` branch, create a new branch for your bug fix:
   ```shell
   git checkout main
   git checkout -b bugfix/update-greeting
   ```

2. **Edit `index.html`**
   - Change the text in `index.html` from **Hello World** to **Hello from your _country_**.

3. **Push Your Branch to Remote**
   - Stage your changes and push the branch to the remote repository:
   ```shell
   git add index.html
   git commit -m "fix: update greeting message"
   git push origin bugfix/update-greeting
   ```

4. **Create a Pull Request on GitHub**
   - Navigate to your GitHub repository and create a pull request from the `bugfix/update-greeting` branch to the `main` branch.

5. **Merge the Branch to Main**
   - Once your pull request is approved, merge it into the `main` branch.

6. **Verify Changes in Main Branch**
   - Update your local `main` branch to verify the changes:
   ```shell
   git checkout main
   git pull
   ```

## Part 2: Bonus Exercise

1. **Create a Feature Branch**
   - From the `main` branch, create another branch named `feat/pull-requests-demo`:
   ```shell
   git checkout main
   git checkout -b feat/pull-requests-demo
   ```

2. **Change the Body Text**
   - Update the body text in `index.html` to:
   ```html
   <body>
     <h1>Hello from Iceland!</h1>
   </body>
   ```

3. **Commit Your Changes**
   - Stage and commit your changes:
   ```shell
   git add index.html
   git commit -m "feat: add Iceland greeting"
   ```

4. **Go Back to Main and Change the Body Text Again**
   - Switch back to the `main` branch and update the body text to:
   ```html
   <body>
     <h1>Hello from Portugal!</h1>
   </body>
   ```
   - Commit your changes:
   ```shell
   git add index.html
   git commit -m "feat: add Portugal greeting"
   ```

5. **Return to Your Feature Branch**
   - Switch back to your feature branch:
   ```shell
   git checkout feat/pull-requests-demo
   ```

6. **Push Your Branch to Remote**
   - Push your feature branch to the remote repository:
   ```shell
   git push origin feat/pull-requests-demo
   ```

7. **Create a Pull Request**
   - Create a pull request from `feat/pull-requests-demo` to `main`.

8. **Check for Merge Conflicts**
   - When attempting to merge, check if you encounter any conflicts. If there are conflicts, resolve them as necessary.

## Additional Resources

For more information on squashing commits, refer to the [Squashing Documentation](../docs/squashing.md).
