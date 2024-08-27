## Branches

A branch represents an independent line of development. It consists series of commits. You can create branch from any other branch or from any commit.
![alt text](../images/branch.png)



**Listing all branches**

```shell
git branch
```

**Creating branches**

```shell
git branch <branch-name>
```

```shell
git checkout -b <branch-name>
```

**Deleting branches**

```shell
git branch -D <branch_name>
```

### Mainline Development

The main motto is to always integrate your changes with everyone's changes. All teammates sontributes to the mainline branch

![Alt text](../images/image.png)

**Pros**

- Easy to track changes because of single branch

**Cons**

- Risk shipping big changes
- less resilient
- need hight quality test environment and QA standards

**Working with multiple branches**

- Feature branch
- develop branch
- hotfix branch
- release branch
- main branch

![Alt text](../images/image-1.png)

### Branching Strategies

**Git flow**

1. Two long running branches (main and develop)
2. Feature braches are cut from develop and merged back to develop
3. New Release branch is cut from the develop which is tested and bugs are fixed in the same branch
4. Merge the release branch back to main
5. Add a tag for the release commit on main and delete the release branch.

![Alt text](../images/image-2.png)

Works well for projects where releases are not very frequent like in case of building librraies

**Github flow**

![alt text](../images/image-31.png)

1. Only one long running branch which is main
2. You cut all the branches feature, bugfix from main
3. Merge the feature branches back to main.

### Branch naming conventions

1. Branch names should be in lowercase.
   `feature/new-login`
2. Use hyphens to separate words
3. Ise alphanumeric characters (0-9)(a-z)
4. Names should be descriptive. You can also include JIRA id in the name
   `feature/T-456-user-auth`

**Branch Prefixes**

Feature branch

```
feature/T-456-user-authentication
```

BugFix

```
bugfix/T-789-fix-header-styling
```

Release

```
release/v2.0.1
```

Hotfix branch

```
hotfix/T-321-security-patch
```

Docs branch

```
docs/T-654-update-readme
```

---

### Moving a commit to another branch

![Alt text](../images/image-3.png)

1. git log and copy the commit hash of the commit you want to move
2. swicth to the branch where you want to move the commit

```
git checkout <branch_name>
git cherry-pick <commit_hash>
```


[Tags](tags.md)
