# Pull Requests

## What are Pull Requests?

Pull requests (PRs) are not a feature of Git itself but are provided by Git hosting platforms like GitHub, GitLab, and Bitbucket. The primary goal of a pull request is to propose changes to the main branch of a project, allowing for discussion and review before merging.

## Problems with Merging Directly to Main

Merging directly into the `main` branch can lead to several issues:

1. **Less Resilient**: Direct merges can introduce instability into the main branch if not properly vetted.
2. **No Way to Get Feedback**: Without a pull request, there’s no structured way for team members to provide feedback on changes.
3. **Conflicts**: Direct merges can lead to conflicts that might not be resolved collaboratively.

## Why Create Pull Requests?

### Collaboration and Code Reviews

Pull requests foster collaboration by allowing team members to review each other's work and provide constructive feedback. This process enhances code quality and ensures that multiple eyes have examined the changes before they are integrated.

- **Invite Feedback**: You can invite others to review your code, suggest improvements, and discuss potential issues.
  
![Pull Request Review](../images/image-4.png)

![Pull Request Approval](../images/image-6.png)

Once your changes have been thoroughly reviewed and approved, your branch can be merged into `main`, ensuring a smooth integration of new features or fixes.

## Additional Resources

For practical experience with pull requests, refer to the [Pull Request Exercise](../exercises/pullRequestExercise.md).
