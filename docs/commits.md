## Commits

Commit is the snapshot of the project taken by git. Snapshots are always committed to the local git repo

![alt text](../images/image-12.png)

### How to create perfect commits ?

1. Create granular commits

   <img src="../images/commit-1.png" width="600" height="300" />

   <img src="../images/commit-2.png" width="600" height="350" />

2. Write valuable commit message
   - A brief and concise subject line that summarizes the changes
   - A descriptive message body that explains the most important facts (and as concisely as possible)
   - using conventional commits

---

<!-- ---

### Undoing commits

```shell
git revert <commit_sha>

git reset <commit_sha> / HEAD~(number of commits back)

git reset --hard <commit_sha>
```

--- -->

### Writing commit messages properly

The **Conventional Commits** specification provides an easy set of rules for writing commit messages properly.

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

**Types with Examples**

1. feat - for new features
2. fix: - for bug fixes
3. Other types ( build:, chore:, refactor:, test:, style: , docs:)
4. BREAKING CHANGE (use ! to draw attention)

**Examples**

```
fix: Resolve issue with user registration
```

```
feat: Add user authentication feature
```

```
refactor: Extract validation helper function
```

```
chore: Clean up unused dependencies
```

**Commit messages with scope**

```
feat(lang): add Polish language
feat(user login): add login form
```

_Use ! to draw attention to a commit_

```
feat!: allow provided config object to extend other configs

BREAKING CHANGE: `extends` key in config file is now used for extending other config files
```

**Commit message with body and footer**

```
feat: Implement user authentication

Add a new feature to allow users to authenticate using email and password.

- Add login form component
- Implement authentication API endpoints
- Store user authentication tokens in local storage

Closes #123

Co-authored-by: Aashima Ahuja <aashi@example.com>
```

**Note**: Use present tense while drafting commit messages like it should be **Implement user authentication** and not **Implemented user authentication**

Further reads

https://www.conventionalcommits.org/en/v1.0.0/

### Amending commits

```shell
git commit -m <commit_message>

git commit --amend -m <new_message>

git commit --amend --no-edit
```

[Commits exercise](../exercises/commitsExercise.md)
