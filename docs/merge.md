# Merging in Git

Merging is a crucial part of collaborating on projects in Git. This guide will walk you through the process of merging feature branches into the main branch and handling merge conflicts.

## Merging a Feature Branch into main

To merge your feature branch into the `main` branch, follow these steps:

1. **Switch to the main Branch**
   ```shell
   git checkout main
   ```

2. **Merge the Feature Branch**
   ```shell
   git merge feature-branch
   ```

> **Note:** It is generally recommended to avoid merging directly into `main`. A better practice is to create a pull request and merge it through platforms like GitHub, GitLab, or Bitbucket.

## Handling Merge Conflicts

If your pull request shows conflicts, you can resolve them in two ways:

### Option 1: Resolve Conflicts via GitHub

- Use the conflict resolution tools provided by GitHub or your chosen platform to resolve conflicts directly in the pull request interface.

### Option 2: Resolve Conflicts Locally

1. **Update Your Local Main Branch**
   ```shell
   git checkout main
   git pull
   ```

2. **Merge Main into Your Feature Branch**
   ```shell
   git checkout feature-branch
   git merge main
   ```

3. **Resolve Conflicts Locally**
   - Open the conflicting files, resolve the conflicts, and then stage the changes:
   ```shell
   git add <resolved_files>
   ```

4. **Complete the Merge**
   ```shell
   git commit -m "fix: resolve merge conflicts"
   ```

## Types of Merges

### Fast-Forward Merge

A fast-forward merge occurs when there are no new commits on the target branch since the feature branch was created. Git simply moves the pointer forward.

![Fast-Forward Merge](../images/image-13.png)

### Three-Way Merge

In cases where both branches have diverged, Git performs a three-way merge. This creates a new commit that reconciles the changes from both branches.

![Three-Way Merge](../images/image-14.png)

## Merge Conflicts

Merge conflicts occur when changes in two branches overlap and Git cannot automatically resolve them. Always review conflicts carefully to ensure that the final code behaves as expected.

### Additional Resources

For more practice with merging, refer to the [Merge Exercise](../exercises/mergingExercise.md).
