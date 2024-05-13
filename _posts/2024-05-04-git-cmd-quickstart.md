---

title: Quick Start - Git Commands
description: Quick Start for Git commands
date: 2024-05-04 08:57:00 -0600
categories: [cmd, devops]
tags: [git, bash]
image:
  path: /assets/img/covers/cover-git.png
  thumbnail: /assets/img/covers/cover-git.png
  alt: "Git"

---

[More GIT Commands]({% link _posts/2024-04-29-git-cmd.md %})

### Install (MacOS)
* `brew install git` -- install Git
* `echo "export PATH=/opt/homebrew/bin:$PATH" >> ~/.zshrc` -- add Homebrew to the PATH

---



### Configure Git Environment
Set configurations that you want to apply to all GIT repositories. To simplify setup and have consistent behavior across projects
* `git config --global user.name "<username>"` -- set global username
* `git config --global user.email "<email address>"` -- set global email
* `git config --edit --global` -- edit global Git configuration

---

### Add a New Repository
1. **Initialize a New Repository:**
   - If you want to create a new repository from scratch:
     ```bash
     git init
     ```
     This command initializes an empty Git repository in your current folder.
2. **Stage Files:**
   - To add files to the staging area for the first commit:
     ```bash
     git add .
     ```
     This stages all new and modified files in the current directory.
3. **Commit Changes:**
   - Create an initial commit:
     ```bash
     git commit -m "Initial commit"
     ```
     This creates a commit with the changes you staged.
4. **Push Initial Commit:**
   - Push the initial commit to the remote repository:
     ```bash
     git push -u origin main
     ```
     This command uploads your changes to the `main` branch on the remote repository.
5. **Check Repository Status:**
   - View the current status of the repository:
     ```bash
     git status
     ```
     This command shows which files are staged, unstaged, or untracked.

---

### Download a Repository
1. `git clone https://github.com/libgit2/libgit2` --downloads a copy of the files
2. `git status` --view status of the repository
3. `git commit -m "adding new folder"` -- commit changes with a message
4. `git push origin main` -- push changes to the main branch