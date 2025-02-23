### Git Workflow

When working with Git, your code exists in four main areas. Understanding these areas is crucial for effective version control.

![Git Workflow Overview](../images/workflow-1.png)

#### Step 1: Clone Your Project from the Remote Repository

To start working on a project, you first need to clone it from the remote repository. This creates a local copy of the project on your machine.

![Cloning a Repository](../images/workflow-2.png)

#### Step 2: Start Working on a File (Working Directory)

The **working directory** is your local development environment where you make changes to your code. This is where you can edit files and test your changes.

![Working Directory](../images/workflow-3.png)

#### Step 3: Add Your Changes to the Staging Area

The **staging area** is a place where you prepare your finalized changes before committing them. You can select which changes to include in the next commit.

![Staging Changes](../images/workflow-4.png)

#### Step 4: Commit Your Changes to Your Local Repository

The `git commit` command takes a snapshot of the staging area and saves it to your local repository. This creates a permanent record of the changes, allowing you to refer back to them later.

![Committing Changes](../images/workflow-5.png)

#### Step 5: Push Your Changes to the Remote Repository

After committing your changes locally, you can use the `git push` command to upload your changes to the remote repository, making them available to your teammates.

![Pushing Changes](../images/workflow-6.png)

---

### Integrating Your Teammate's Work

To incorporate changes made by your teammates, you can use the `git pull` command. This fetches and merges changes from the remote repository into your local repository.

![Pulling Changes](../images/workflow-7.png)
![Integrating Changes](../images/workflow-8.png)

---

### Additional Resources

- [Git Setup Instructions](setup.md)
