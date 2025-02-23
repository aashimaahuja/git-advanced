# Interactive Rebase Exercise

In this exercise, you will practice using interactive rebase in Git. Follow the instructions below:

## Tasks

1. **Squash the Last Two Commits**
   - Use interactive rebase to combine the last two commits into a single commit.
   - Command:
     ```shell
     git rebase -i HEAD~2
     ```
   - In the editor, change `pick` to `squash` for the second commit.

2. **Delete a Commit**
   - Use interactive rebase to remove a specific commit from your history.
   - Command:
     ```shell
     git rebase -i HEAD~3
     ```
   - In the editor, change `pick` to `drop` or simply remove the line corresponding to the commit you want to delete.

## Additional Resources

For further reading and practice, refer to the [Take Home Assignment](../assignment.md).
