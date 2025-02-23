# Branch Exercise

This exercise will guide you through the process of creating and managing branches in Git while developing a user authentication feature. Follow the steps outlined in each part carefully.

## Part 1: Developing the User Authentication Feature

You are tasked with developing a user authentication feature. Please follow the steps below:

1. **Create a Feature Branch**
   - Use the following command to create a feature branch following the naming conventions:
   ```shell
   git checkout -b feature/T-456-user-authentication
   ```

2. **Create Required Files**
   - Create the following files in your project directory:
     - `authentication.js`
     - `LoginForm.html`

3. **Make a Commit**
   - After making changes to the files, stage them and commit using conventional commit messages:
   ```shell
   git add authentication.js LoginForm.html
   git commit -m "feat(auth): add user authentication feature"
   ```

## Part 2: Bug Fixing

1. **Create a Separate Branch for Bug Fixes**
   - From the GitHub UI, create a new branch for fixing bugs in the authentication feature. Use a descriptive branch name, such as:
   ```
   bugfix/T-789-fix-authentication-issue
   ```

2. **Make a Commit**
   - In this new bugfix branch, make the necessary changes to resolve the issue and commit your changes:
   ```shell
   git add <modified_files>
   git commit -m "fix(auth): resolve authentication issue"
   ```

3. **Cherry-Pick the Commit**
   - Switch back to your feature branch and cherry-pick the commit you made in the bugfix branch:
   ```shell
   git checkout feature/T-456-user-authentication
   git cherry-pick <commit_hash>
   ```

### Additional Resources

For more information on merging branches, refer to the [Merging Documentation](../docs/merge.md).
