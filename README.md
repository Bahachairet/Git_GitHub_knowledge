# Git/GitHub Cheatsheet

Welcome to this Git/GitHub cheatsheet! Whether you're a seasoned developer or just starting out, this guide will help you navigate the most common Git commands and GitHub workflows. Let's dive in!

## Basic Git Commands

### Initialize a Repository

To start a new Git repository in an existing directory:

```bash
git init
```

This initializes a `.git` directory, which is where Git stores all your project's version control information.

### Clone a Repository

To copy an existing repository from a remote location:

```bash
git clone https://github.com/username/repository.git
```

This command creates a local copy of the repository, including all files, branches, and commit history.

### Check Repository Status

To see the current status of your repository:

```bash
git status
```

This command shows which files have been modified, staged, or are ready to be committed.

### View Changes

To see the differences between your working directory and the staging area:

```bash
git diff
```

For example, if you've made changes to `index.html`:

```bash
git diff index.html
```

### Add Changes to Staging

To stage changes for the next commit:

```bash
git add index.html
```

Or, to stage all changes in the directory:

```bash
git add .
```

### Commit Changes

To commit staged changes to the repository:

```bash
git commit -m "Initial commit"
```

Commit messages should be clear and concise, describing the changes made.

### View Commit History

To view the commit history:

```bash
git log
```

For a condensed view:

```bash
git log --oneline
```

## Branching and Merging

### List Branches

To see all local branches:

```bash
git branch
```

### Create a New Branch

To create a new branch without switching to it:

```bash
git branch feature-branch
```

### Switch to a Branch

To switch to an existing branch:

```bash
git checkout feature-branch
```

Or, using the newer `switch` command:

```bash
git switch feature-branch
```

### Create and Switch to a New Branch

To create a new branch and switch to it in one step:

```bash
git checkout -b feature-branch
```

Or:

```bash
git switch -c feature-branch
```

### Merge a Branch

To merge a branch into the current branch:

```bash
git merge feature-branch
```

### Delete a Branch

To delete a branch:

```bash
git branch -d feature-branch
```

Use `-D` to force delete a branch that hasn't been merged yet.

## Remote Repositories

### Add a Remote

To add a remote repository:

```bash
git remote add origin https://github.com/username/repository.git
```

### List Remotes

To view all remote repositories associated with your local repository:

```bash
git remote -v
```

### Push Changes to Remote

To push your commits to a remote repository:

```bash
git push origin main
```

Replace `main` with the name of the branch you want to push.

### Pull Changes from Remote

To fetch and merge changes from a remote repository:

```bash
git pull origin main
```

### Fetch Changes

To fetch changes from a remote repository without merging:

```bash
git fetch origin
```

## Stashing and Undoing

### Stash Changes

To temporarily save changes that aren't ready to be committed:

```bash
git stash
```

### List Stashes

To see all stashed changes:

```bash
git stash list
```

### Apply Last Stash

To reapply the most recent stash:

```bash
git stash apply
```

### Drop a Stash

To remove a stash:

```bash
git stash drop
```

### Undo Last Commit

To undo the last commit but keep the changes:

```bash
git reset --soft HEAD~1
```

To undo the last commit and discard changes:

```bash
git reset --hard HEAD~1
```

## Tagging

### Create a Tag

To create a lightweight tag:

```bash
git tag v1.0.0
```

For an annotated tag:

```bash
git tag -a v1.0.0 -m "Version 1.0.0 release"
```

### Push Tags to Remote

To push a single tag:

```bash
git push origin v1.0.0
```

To push all tags:

```bash
git push origin --tags
```

### Delete a Tag

To delete a local tag:

```bash
git tag -d v1.0.0
```

To delete a remote tag:

```bash
git push origin --delete v1.0.0
```

## GitHub Specific

## Configuration

### Set Global Username and Email

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

### View Configuration

```bash
git config --list
```


