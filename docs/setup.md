#### Setting up Git

**Downloading Git**

Git is already installed in Mac OS. Check with command

```
git --version
```

Windows users can install git from this link
https://git-scm.com/download/win

**Git config setup**

Add your name and email in git config file (.gitconfig)

```
git config --global user.name "Aashima Ahuja"

git config --global user.email "aashima@gmail.com"

```

You can check the contents of your .gitconfig file by opening it like

```
vi ~/.gitconfig
```

or

```
code ~/.gitconfig
```

You can change the contents directly by opening this file in vim or code.

If you are unsure about the gitconfig path , check it by this command

```
git config --list --show-origin
```

**Initialising a git repository**

- Git init in the project
- .git folder is created inside the project
- git will start tracking your project files

**Pushing existing project to github**

Add remote

```
git remote add <remote_name> <remote_url>
```

Push branch to remote

```
git push -u <remote_name> <branch_name>
```

Check if the remote has been added

```
git remote -v
```

By default remote name is kept as origin. If you want to change the remote name, use

```
git remote rename <old_remote_name>
<new_remote_name>

```
