## Undo mistakes in Git

<div style="display:flex; flex-direction:column; gap:16px">
<details>

<summary>You want to discard uncommitted changes in a file. 
</summary>
  
```
git restore <filename>
```
</details>

<details>

<summary>
You accidently deleted a file and want to restore it back. 
</summary>
  
```
git restore <filename>
```
</details>

<details>

<summary> 
You made a typo in your commit message
</summary>
  
```
git commit --amend -m <new_message>
```

*Note: Amending commits changes the hash which means its entirely new commit. So don't amend if you have pushed to the remote*

</details>

<details>

<summary>You made a commit and forgot to include one file
</summary>
  
```
git add <forgotten_filename>

git commit --amend --no-edit
```
</details>

<details>

<summary>You were doing some code rafactoring. However the code didn't work properly. So now you want to discard everything and go back the previous state of the project.</summary>
  
```
git reset --hard HEAD
```
</details>

<details>

<summary>
You made some commits to the repo and now you want to remove them.

![Alt text](image-1.png)

</summary>
  
```
git reset --hard <commit_hash>
```
</details>

<details>

<summary>
You have accidently made a commit to the main branch which you actually wanted to do in the feature branch.

</summary>
  

*Move commit from master to the feature branch*

```
git checkout <feature_branch>
git cherry-pick <commit_hash>
```

*Remove commit from main*

```
git reset --hard HEAD~1
```

</details>

<details>

<summary>
You made a commit. Did reset hard and now you lost that commit. You have realised that this was not the brightest idea and now you are in panic ! 
</summary>
  
```
git reflog
```
Find hash one previous to reset command and run either

```
git reset --hard <hash>
```
or

```
git branch <branch_name> hash
```

</details>

<details>

<summary>
You accidentally deleted a feature branch and realised that you still needed it.
</summary>
  
```
git reflog
```
Find the commit with feature branch and run

```
git branch <branch_name> <hash>
```
</details>
</div>
