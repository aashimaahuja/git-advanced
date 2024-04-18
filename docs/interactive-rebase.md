### Powers of Interactive Rebase

_Interactive rebase allows you to rewrite the commit history. You can_

- change commit messages
- combine multiple commits
- split and edit existing commits
- reorder commits
- delete commits

#### Change a commit message

**_Using ammend_**

```shell
git commit --amend
```

_With amend you can only amend last commit_

**_Using Interactive rebase_**

```shell
git rebase -i HEAD~3
```

use reword to change the commit message

![Alt text](../images/image-18.png)

#### Combine two commits

```shell
git rebase -i HEAD~3
```

![Alt text](../images/image-19.png)

#### Delete a commit

```shell
git rebase -i HEAD~3
```

![Alt text](../images/image-20.png)
