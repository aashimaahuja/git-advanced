### Create Repo Exercise

In this exercise, you will create a new project named **git-workshop** and perform some basic Git operations. Follow the instructions below:

#### Part 1: Setting Up the Project

1. **Create a New Project**: 
   - Create a new directory named `git-workshop`.

2. **Create Files**: 
   - Inside the `git-workshop` directory, create two files with the following contents:

   - **`index.html`**:

     ```html
     <!DOCTYPE html>
     <html lang="en">
       <head>
         <title>Hello, World!</title>
       </head>
       <body>
         <h1>Hello, World!</h1>
       </body>
     </html>
     ```

   - **`styles.css`**:

     ```css
     body {
       font-family: Arial, sans-serif;
       background-color: #f0f0f0;
       color: #333;
       margin: 0;
       padding: 0;
     }
     ```

3. **Commit the Files**: 
   - Use the following commands to stage and commit the files:

     ```shell
     git add index.html styles.css
     git commit -m 'feat: First Commit'
     ```

4. **Push the Project to GitHub**: 
   - Ensure you have set up a remote repository on GitHub and push your project:

     ```shell
     git push -u origin main
     ```

---

#### Part 2: Updating the Project

1. **Change the Remote Name**: 
   - Change the remote name from `origin` to `base` using the following command:

     ```shell
     git remote rename origin base
     ```

2. **Update the `index.html` File**: 
   - Modify the `index.html` file to the following content:

     ```html
     <!DOCTYPE html>
     <html lang="en">
       <head>
         <title>Hello, World!</title>
       </head>
       <body>
         <h1>Welcome to the Git Course</h1>
       </body>
     </html>
     ```

3. **Commit the Changes**: 
   - After updating the file, commit your changes:

     ```shell
     git add index.html
     git commit -m 'fix: Update welcome message'
     ```

4. **Push the Changes**: 
   - Push the updated file to the remote repository:

     ```shell
     git push base main
     ```

5. **Change the Remote Name Back to Origin**: 
   - Rename the remote back to `origin`:

     ```shell
     git remote rename base origin
     ```

6. **Verify the Remote Name**: 
   - Check if the remote has been changed back to `origin` by running:

     ```shell
     git remote -v
     ```

---

### Additional Resources

- [Git Basic Commands](../docs/basic-commands.md)
