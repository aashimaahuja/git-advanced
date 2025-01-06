## Reflog

1. Recover lost commits

<details>

<summary>
You made a commit. Did reset hard and now you lost that commit. You have realised that this was not the brightest idea and now you are in panic !
</summary>

```shell
git reflog
```

Find hash one previous to reset command and run either

```shell
git reset --hard <hash>
```

or

```shell
git branch <branch_name> hash
```

</details>

2. Recover accidently deleted branch

<details>

<summary>
You accidentally deleted a feature branch and realised that you still needed it.
</summary>

```shell
git reflog
```

Find the commit with feature branch and run

```shell
git branch <branch_name> <hash>
```

</details>
