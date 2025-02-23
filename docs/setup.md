## Setting Up Git

Setting up Git is essential for effective version control. Follow these steps to get started:

### 1. Downloading Git

- **Mac OS**: Git is pre-installed. You can check the installation with the following command:

  ```shell
  git --version
  ```

- **Windows**: Download and install Git from the following link: [Git for Windows](https://git-scm.com/download/win).

### 2. Git Configuration Setup

You need to configure your Git environment by adding your name and email to the Git config file (`.gitconfig`):

```shell
git config --global user.name "Penchal Naidu"
git config --global user.email "PenchalNaiduModhepalli@gmail.com"
```

To check the contents of your `.gitconfig` file, you can open it using:

```shell
vi ~/.gitconfig
```

or

```shell
code ~/.gitconfig
```

You can change the contents directly by editing this file in your preferred text editor(say vim or Visual Studio Code Or Eclipse or IntelliJ IDEA
).

If you are unsure about the path of the Git config file, you can check it with the following command:

```shell
git config --list --show-origin
```

### 3. Initializing a Git Repository

To start tracking your project files, navigate to your project directory and run:

```shell
git init
```

This command creates a `.git` folder inside your project, enabling Git to track your files.

### 4. Adding a `.gitignore` File

Create a `.gitignore` file in the root of your project. Any files or directories specified in this file will not be tracked by Git.

---

### Pushing Project to Remote (GitHub Server)

#### 1. Pushing an Existing Project to GitHub

- **Add Remote**: To link your local repository to a remote repository, use:

  ```shell
  git remote add <remote_name> <remote_url>
  ```

- **Push Branch to Remote**: To push your changes to the remote repository, run:

  ```shell
  git push -u <remote_name> <branch_name>
  ```

- **Check Remote**: To verify if the remote has been added successfully, use:

  ```shell
  git remote -v
  ```

By default, the remote name is set to `origin`. If you want to change the remote name, use:

```shell
git remote rename <old_remote_name> <new_remote_name>
```

#### 2. Cloning a Project from GitHub

To clone an existing repository from GitHub, use:

```shell
git clone <remote_repo_url>
```

### Shell Theme

For a better terminal experience, consider using the Powerline9k theme. You can find setup instructions here: [Powerline9k Setup](https://blog.woodies11.dev/how-i-set-up-my-terminal-oh-my-zsh-powerline9k-iterm-2/).

---

### Additional Resources

- [Create Repo Exercise](../exercises/creatingRepoExercise.md)
