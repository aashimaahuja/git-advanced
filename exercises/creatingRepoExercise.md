Create a new project named **git-workshop**. Create two files in it with follwing contents

_index.html_

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

_styles.css_

```css
body {
  font-family: Arial, sans-serif;
  background-color: #f0f0f0;
  color: #333;
  margin: 0;
  padding: 0;
}
```

Commit the files using

```
git add index.html styles.css
git commit -m 'feat: First Commit'
```

Push the project on github.

**Part 2**

1. Change the remote name from _origin_ to _base_
2. Update the index.html file

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Hello, World!</title>
  </head>
  <body>
    <h1>welcome to git course</h1>
  </body>
</html>
```

3. Commit the file and do

```
git push base
```

4. Change the remote name back to origin. Verify if the remote is changed back to origin.

[Git Basic Commands](/docs/basic-commands.md)
