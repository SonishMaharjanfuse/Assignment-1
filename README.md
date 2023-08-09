# Git Basics and Pre-Commit Hook Usage

Welcome to the Git Basics and Pre-Commit Hook Usage guide! This README provides an overview of Git, its essential commands, and instructions on setting up and using a pre-commit hook for enhancing code quality in your Git repository.

## Table of Contents

1. [Git Introduction](#git-introduction)
2. [Git Commands](#git-commands)
   - [git init](#git-init)
   - [git clone](#git-clone)
   - [git add](#git-add)
   - [git commit](#git-commit)
   - [git push](#git-push)
   - [git pull](#git-pull)
3. [Using Pre-Commit Hooks](#using-pre-commit-hooks)
   - [Setting Up a Pre-Commit Hook](#setting-up-a-pre-commit-hook)
   - [Customizing the Pre-Commit Hook](#customizing-the-pre-commit-hook)
   - [Example Pre-Commit Hook](#example-pre-commit-hook)
4. [Reference](#reference)

## Git Introduction

Git is a distributed version control system that enables developers to track changes to source code over time. It helps teams collaborate, manage different versions of code, and maintain project history.

## Git Commands

### `git init`

Initialize a new Git repository in the current directory: <br>

### `git clone`

Clone a remote repository to your local machine: <br>
git clone <repository_url>

### `git add`
Stage changes for commit:<br>
git add <file_name>

### `git commit`
Create a commit to save staged changes:<br>
git commit -m "Commit message"

### `git push`
Push local commits to a remote repository:<br>
git push origin <branch_name>

### `git pull`
Pull remote changes to your local repository:<br>
git pull origin <branch_name>

## Using Pre-Commit Hooks
Setting Up a Pre-Commit Hook<br>
A pre-commit hook is a script that runs before a commit is made. It helps enforce code quality standards before changes are committed.<br>

Navigate to the root of your repository.<br>

Inside the .git/hooks directory, create a file named pre-commit (without an extension).<br>

### Make the file executable:
chmod +x .git/hooks/pre-commit

### Customizing the Pre-Commit Hook
Edit the pre-commit script to add checks or tests that you want to run before each commit. For example, you can run linters, tests, or other code analysis tools.


#### #Read the commit message from the file
commit_msg=$(cat "$commit_msg_file")

#### #Check the commit type in the commit message
check_commit_type "$commit_msg"

## Reference
<a href='https://www.atlassian.com/git/tutorials/git-hooks'>Git hooks</a><br>
<a href='https://www.atlassian.com/git/tutorials/what-is-version-control#:~:text=Version%20control%2C%20also%20known%20as,to%20source%20code%20over%20time.'>Version Control</a>
