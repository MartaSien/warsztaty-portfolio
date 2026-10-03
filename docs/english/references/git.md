---
icon: simple/git
---

# Git in 5 Minutes


## Commands


Run commands in the terminal while you are in your repository folder.


| Command | Description |
| --- | --- |
| `git status` | Shows the repository status: modified, new, and staged files |
| `git log` | Shows the commit history <br>`--oneline` - only the latest commit |
| `git add file-name` | Stages a specific file for commit |
| `git add .` | Stages all modified files for commit |
| `git commit -m "Description of changes"` | Saves staged changes in the repository history |
| `git diff` | Shows changes that have not yet been added with `git add` |
| `git branch` | Displays the list of branches |
| `git switch branch-name` | Switches to the specified branch |
| `git switch -c branch-name` | Creates a new branch and immediately switches to it |
| `git help command-name` | Opens help for the selected command, e.g. `git help commit` |


## Examples


### Create a commit


Creates a commit containing all changes in the repository.


```bash
git status
git add .
git commit -m "Description of changes"
```