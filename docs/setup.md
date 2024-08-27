## Setting up Git

**1. Downloading Git**

Git is already installed in Mac OS. Check with command

```shell
git --version
```

Windows users can install git from this link
https://git-scm.com/download/win

**2. Git config setup**

Add your name and email in git config file (.gitconfig)

```shell
git config --global user.name "Aashima Ahuja"

git config --global user.email "aashima@gmail.com"

```

You can check the contents of your .gitconfig file by opening it like

```shell
vi ~/.gitconfig
```

or

```shell
code ~/.gitconfig
```

You can change the contents directly by opening this file in vim or code.

If you are unsure about the gitconfig path , check it by this command

```shell
git config --list --show-origin
```

**3. Initialising a git repository**

- Git init in the project
- .git folder is created inside the project
- git will start tracking your project files

**4. Adding `.gitignore` file**

Create `.gitignore` file in root of your project. The files or directories mentioned in `.gitignore` will not be tracked

---

### Pushing project to remote (github server)

**1.Pushing existing project to github**

Add remote

```shell
git remote add <remote_name> <remote_url>
```

Push branch to remote

```shell
git push -u <remote_name> <branch_name>
```

Check if the remote has been added

```shell
git remote -v
```

By default remote name is kept as origin. If you want to change the remote name, use

```shell
git remote rename <old_remote_name>
<new_remote_name>

```

**2. Cloning project from github**

`git clone <remote_repo_url>`


[Create Repo Exercise](../exercises/creatingRepoExercise.md)
