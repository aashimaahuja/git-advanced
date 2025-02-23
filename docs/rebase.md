# Rebase in Git

Rebasing is a powerful feature in Git that allows you to integrate changes from one branch into another by replaying commits. This results in a cleaner project history without merge commits.

## How to Rebase

To rebase your feature branch onto `main`, follow these steps:

1. **Checkout Your Feature Branch**
   - Start by checking out the feature branch you want to rebase:
   ```shell
   git checkout featureA
   ```

2. **Rebase onto Main**
   - Run the rebase command to apply your feature branch changes on top of the latest `main` branch:
   ```shell
   git rebase main
   ```

![Rebase Example](../images/image-15.png)

### Benefits of Rebasing

- **Clean History**: With rebasing, there are no merge commits, resulting in a linear and clean project history. This makes it easier to follow the evolution of the codebase.

## Pitfalls of Rebasing

- **Avoid Rebasing Shared Commits**: Be cautious when rebasing commits that exist outside your local repository. If others have based their work on those commits, rebasing can lead to confusion and conflicts.
  
![Rebase Pitfall](../images/image-16.png)

## Additional Resources

For more practice with rebasing, refer to the [Rebase Exercise](../exercises/rebaseExercise.md).
