# Creating Tags

Tags are a powerful feature in Git, typically used to mark release points (e.g., v1.0, v2.0). This document outlines how to create, list, display, and delete tags in your Git repository.

## Listing Tags

To view all existing tags in your repository, use the following command:

```shell
git tag
```

## Creating Tags

### Annotated Tags

Annotated tags are stored as full objects in the Git database. They include the tagger's name, email, date, and a message. To create an annotated tag, run:

```shell
git tag -a v1.0 -m 'My first version'
```

### Lightweight Tags

Lightweight tags are essentially bookmarks to a specific commit. They do not contain additional information. To create a lightweight tag, use:

```shell
git tag v1.0
```

## Displaying Tag Information

To view detailed information about a specific tag, including the commit it points to, use:

```shell
git show v1.0
```

## Deleting Tags

If you need to delete a tag, you can do so with the following command:

```shell
git tag --delete <tag_name>
```

### Example

To delete an annotated tag named `v1.0`:

```shell
git tag --delete v1.0
```

---

### Additional Resources

- For more information on merging, see the [Merging Documentation](../docs/merge.md).

By utilizing tags effectively, you can manage your releases and milestones with greater clarity and organization. Feel free to reach out if you have any questions or need further assistance!
