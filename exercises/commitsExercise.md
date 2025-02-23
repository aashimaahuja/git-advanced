# Commits Exercise

This exercise will guide you through the process of making commits in Git, amending them, and adding new files to existing commits.

## Exercise Steps

### 1. Make a Commit

Start by creating a new file and making your first commit. For example, let's create a file named `hello_world.py`.

```shell
echo 'print("Hello, World!")' > hello_world.py
git add hello_world.py
git commit -m "feat: Add hello world script"
```

### 2. Amend Commit Using a Conventional Commit Message

Suppose you realize that you need to enhance the `hello_world.py` file by adding a function to greet a user. After making the changes, you can amend the previous commit instead of creating a new one.

**Modify the file:**

```python
def greet(name):
    return f"Hello, {name}!"

if __name__ == "__main__":
    print(greet("World"))
```

**Amend the commit:**

```shell
git add hello_world.py
git commit --amend -m "feat: Enhance hello world script with greeting function"
```

### 3. Create a New File and Add It to the Same Commit

Now, let’s say you want to add a README file that explains the purpose of the `hello_world.py` script. You can create this file and add it to the same commit.

**Create the README file:**

```shell
echo '# Hello World Script' > README.md
echo 'This script prints a greeting message.' >> README.md
```

**Add and amend the commit:**

```shell
git add README.md
git commit --amend -m "docs: Add README for hello world script"
```

### Summary of Commands

- **Creating a new file**: `echo '...' > filename`
- **Adding files to staging**: `git add filename`
- **Making a commit**: `git commit -m "message"`
- **Amending a commit**: `git commit --amend -m "new message"`

### Additional Resources

For more information on undoing changes in Git, refer to the [Undoing Changes in Git](../docs/undoing-changes.md) document.

---

### Practice Exercise

Now that you've completed the initial exercise, try the following:

1. **Create a new feature**: Implement a new function in `hello_world.py` that takes user input for their name and greets them.
2. **Make a commit for this feature** using a conventional commit message.
3. **Add unit tests** for your function in a new file named `test_hello_world.py` and amend your previous commit to include these tests.

This will help reinforce your understanding of committing changes and using Git effectively!
