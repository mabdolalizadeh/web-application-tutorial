# Git Notes

## Introduction to Git
Git is a distributed version control system that helps track changes in source code during software development. It allows multiple developers to work on a project simultaneously and manage different versions of the code efficiently.

## Installing Git
### Windows
1. Download Git from [git-scm.com](https://git-scm.com/)
2. Run the installer and follow the default settings
3. Open Git Bash to start using Git

### Linux
1. Open the terminal and run:
   ```sh
   sudo apt update
   sudo apt install git
   ```
2. Verify installation with:
   ```sh
   git --version
   ```

### macOS
1. Install Git via Homebrew:
   ```sh
   brew install git
   ```
2. Verify installation:
   ```sh
   git --version
   ```

## Configuring Git
Set up your user information:
```sh
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
```
To check your configurations:
```sh
   git config --list
```

## Basic Git Commands

### Initializing a Repository
Create a new repository:
```sh
   git init
```
> [!NOTE]
> repository is a git space.

Clone an existing repository:
```sh
   git clone <repository_url>
```
> [!TIP]
> we have some spaces for share repos online. such as [github](github.com) or [gitlab](gitlab.com) and etc. </br> we use `git clone` to copy a repo from a space like github.

### Making Changes
Check the status of the repository:
```sh
   git status
```
Add files to the staging area:
```sh
   git add <file>
   git add .  # Add all changes
```
Commit changes:
```sh
   git commit -m "Your commit message"
```

### Branching
Create a new branch:
```sh
   git branch <branch_name>
```
Switch to a branch:
```sh
   git checkout <branch_name>
```
Create and switch to a new branch:
```sh
   git checkout -b <branch_name>
```

### Merging Branches
Merge a branch into the current branch:
```sh
   git merge <branch_name>
```
Resolve merge conflicts manually if required.

### Remote Repositories
Add a remote repository:
```sh
   git remote add origin <repository_url>
```
Push changes to the remote repository:
```sh
   git push origin <branch_name>
```
Pull the latest changes from the remote repository:
```sh
   git pull origin <branch_name>
```

### Undoing Changes
Undo changes in the working directory:
```sh
   git checkout -- <file>
```
Reset the last commit:
```sh
   git reset --soft HEAD~1  # Keep changes staged
   git reset --mixed HEAD~1 # Keep changes but unstage
   git reset --hard HEAD~1  # Discard changes
```

### Viewing History
Check commit history:
```sh
   git log
```
View changes:
```sh
   git diff
```

# Git Tasks
- sign up in github and make a repo in it.
- clone the repo in ur system and change files
- push origin to master
- in github change files and then pull it to system
