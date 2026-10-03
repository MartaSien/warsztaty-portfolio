# Lesson 2: Git and advanced Pelican features

## Why do developers use Git?

> [A brief introduction to Git for beginners | GitHub](https://www.youtube.com/watch?v=r8jQ9hVA2qs)
Git is the most well-known version control system (though not the only one).
Imagine having access to a file's entire history instead of just an "undo" command. You could check:

> - who made a specific change
> - what the file looked like `n` operations ago
> - why the file was changed

Developers use Git to:

- track the history of changes in files
- access older versions of files
- collaborate with others on the same file simultaneously
- save multiple variants of the same project

## Introduction

### Opening our `my-portfolio` repository.

### Creating a new branch and making changes on it

```
git branch "initial-website"
```

### Creating a .gitignore file

The `.gitignore` file is used to specify files and folders that we do not want to share with others—such as cache files, secrets, or local settings. Changes to these files will not be tracked by `git`.

??? info ".gitignore"
```bash
__pycache__
```

Here, we create a commit just as before. ### Merging changes into the main branch

Switch to the main branch:

```bash
git switch master
```

Merge changes from the `initial-python-script` branch:

```bash
git merge initial-python-script
```

Check the commit history:

```bash
git log
```

After a successful merge, the working branch is no longer needed, so we can delete it:

```bash
git branch -d initial-python-script
```

### Reverting a change we don't want in the repo

`git revert` does not delete history. It creates a new commit that reverses the changes from a specific commit.

First, check the commit ID:

```bash
git log
```

Then, revert the selected commit:

```bash
git revert <commit-id>
```

Example:

```bash
git revert a1b2c3d
```

### Useful extensions

- [LiveShare](https://visualstudio.microsoft.com/services/live-share/) - allows you to share your Visual Studio Code session with others and collaborate on a single file.
- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) - displays change history, code line authors, and commit information directly within the editor.