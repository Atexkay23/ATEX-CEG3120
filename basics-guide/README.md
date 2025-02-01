# Basics Guide
References for basic Git and GitHub commands
 ## Table of Contents
- [Basics Guide](#basics-guide)
- [Command Line Git](#command-line-git)
  - [git status](#git-status)
  - [git log](#git-log)
  - [git clone](#git-clone)
- [Git Files & Folders](#git-files--folders)
- [GitHub](#github)
- [SSH](#ssh)
- [Resources](#resources)
## Command  Line Git
### git status
- **Description**: Shows the status of the local repository, such as uncommitted changes, staged files, and untracked files.
- **Usage**:  ```bash git status ```

### git log
- **Description**: Displays the commit history.
- **Usage**:  ```bash git log ```

### git clone
- **Description**: Clones a remote repository to your local machine.
- **Usage**:  ```bash git clone https://github.com/username/repository.git ```

### git add
- **Description**: Stages files for commit.
- **Usage**:  ```bash git add <file_name> ```
- **Explanation**: This command stages a file (or files) to be included in the next commit. You can add specific files or use `git add .` to add all modified files.

### git rm
- **Description**: Removes files from the staging area and/or working directory.
- **Usage**:  ```bash git rm <file_name> ```
- **Explanation**: This removes a file from the staging area and working directory (i.e., deletes it). To **untrack** a file (keep it locally but not in the repository), use:  ```bash git rm --cached <file_name> ```

### git commit
- **Description**: Commits staged changes to the repository.
- **Usage**:  ```bash git commit -m "Your commit message" ```
- **Explanation**: This command commits all the changes staged by `git add` and includes a message describing the changes.

### git push
- **Description**: Pushes local commits to the remote repository.
- **Usage**:  ```bash git push origin main ```

### git fetch
- **Description**: Fetches changes from the remote repository without merging them.
- **Usage**:  ```bash git fetch origin ```
- **Explanation**: This downloads changes from the remote repository, but it does not automatically merge them with your local branch. You can inspect the changes before deciding to merge.

### git merge
- **Description**: Merges changes from one branch into another.
- **Usage**:  ```bash git merge <branch_name> ```
- **Explanation**: Merges the changes from the specified branch into the current branch. For example, if you are on the `main` branch and want to merge changes from `feature-branch`, you would run `git merge feature-branch`.

### git pull
- **Description**: Fetches and merges changes from the remote repository into your local branch.
- **Usage**:  ```bash git pull origin main ```

### git branch
- **Description**: Lists, creates, or deletes branches.
- **Usage**:  ```bash git branch ```
To create a new branch:  ```bash git branch <branch_name> ```

### git tag
- **Description**: Adds a tag to a specific commit.
- **Usage**:  ```bash git tag <tag_name> ```
- **Explanation**: Tags are often used to mark specific points in the history, such as releases.

### git checkout
- **Description**: Switches between branches or restores files.
- **Usage**:  ```bash git checkout <branch_name> ```
To switch to a specific branch, use `git checkout <branch_name>`. To restore a file, use:  ```bash git checkout -- <file_name> ```

### git init
- **Description**: Initializes a new Git repository.
- **Usage**:  ```bash git init ```
- **Explanation**: This command creates a new `.git` directory in your project folder, making it a Git repository.

### git remote
- **Description**: Manages remote repositories.
- **Usage**:  To view remotes:  ```bash git remote -v ```
To add a remote:  ```bash git remote add origin https://github.com/username/repository.git ```
- **Explanation**: This command allows you to configure and interact with remote repositories. You can add, remove, or change the remotes associated with your local repository.

## Git Files & Folders

### .git folder
- **Description**: The `.git` folder is created in the root directory of every Git repository. This folder contains all the configuration files, information about the repository’s history, branches, remotes, and much more. It is a hidden folder and should not be manually edited. It stores the complete history and metadata for the repository.
- **Purpose**: The `.git` folder is what turns a project folder into a Git repository. If you delete this folder, you lose all the versioning and history for the project.

### .gitignore file
- **Description**: The `.gitignore` file tells Git which files or directories to ignore in a project. This can be used to prevent certain files (such as build files, configuration files, or log files) from being tracked by Git.
- **Usage**: You simply add the file paths or patterns to the `.gitignore` file, and Git will exclude those from version control.
- **Example**:
  ```bash
  # Ignore all .log files
  *.log

  # Ignore node_modules folder
  node_modules/

  # Ignore all files in the tmp directory
  tmp/*

#!/bin/bash

## GitHub Pull Request Process

### Step 1: Fork or clone the repository (replace <repo-url> with the URL of the repo)
echo "Cloning repository..."
git clone <repo-url>
cd <repo-name> # Change to your repo folder

### Step 2: Create a new branch
echo "Creating a new branch..."
git checkout -b <new-branch-name>

### Step 3: Make changes (this part is manual - edit files as needed)

### Step 4: Add the changes to the staging area
echo "Adding changes..."
git add .

### Step 5: Commit the changes
echo "Committing changes..."
git commit -m "Description of changes"

### Step 6: Push changes to the remote repository
echo "Pushing changes to remote repository..."
git push origin <new-branch-name>

### Step 7: Open the repository on GitHub and create a Pull Request
### You can't fully automate this process without the GitHub API, so this step will open GitHub in the browser
echo "Opening GitHub repository in browser to create Pull Request..."
open "https://github.com/<username>/<repo-name>/pulls" # Open the PR page in the browser


