---
title: Git Tutorials
description: Git tutorials for beginners
date: 2024-07-14 10:00:00 -0600
categories: [ci/cd,cmd]
tags: [git,github]
image:
  path: /assets/images/covers/cover-git-tutorials.png
  thumbnail: /assets/images/covers/cover-git-tutorials.png
  alt: "Git Tutorials - for beginners"
media_subpath: /assets/images/

---
Path to this page: {{ page.path }}
[Git Commands Page]({% link {{ page.path }}%})

## Download a Repository

```bash
git clone https://github.com/<your repo>  #downloads a copy of the files
git status #view status of the repository
git commit -m "adding new folder" #commit changes with a message
git push origin main` #Upload your local commits to the main branch of remote repository.
```

---

## Initialize a New Repository

**1. Initialize:**

- To create a new repository from scratch, this command initializes an empty Git repository in your current folder.

```bash
git init
```

**2. Stage Files:**

- To add files to the staging area for the first commit, this command stages all new and modified files in the current directory.

```bash
git add .
```

**3. Commit Changes:**

- This creates a commit with the changes you staged.

```bash
git commit -m "Initial commit"
```

**4. Push Initial Commit:**

- To push the initial commit to the remote repository, this command uploads your changes to the main branch on the remote repository.

```bash
git push -u origin main
```

**5. Check Repository Status:**

- To view the current status of the repository, this command shows which files are staged, unstaged, or untracked.

```bash
git status
```

---

## Fix Conflict - Sync locals repos with remote GIT repository

To ensure that both Machine A and Machine B are synchronized with the remote Git repository after resolving conflicts.

### Sync Mac A and Mac B with Remote GIT

1. **Force Push from Machine A**:
   First, ensure that Machine A's local repository state is pushed to the remote repository on GitHub, potentially overwriting the remote repository with the local changes.

   ```sh
   cd ~/dotfiles
   git add .
   git commit -m "Ensure local changes are up to date"
   git push origin main --force
   ```

2. **Fetch and Reset on Machine B**:
   Next, on Machine B, fetch the latest changes from the remote repository and reset the local repository to match the remote state. This will discard any local changes on Machine B that are not in the remote repository.

   ```sh
   cd ~/dotfiles
   git fetch origin
   git reset --hard origin/main
   ```

3. **Pull Latest Changes on Machine A** (Optional but recommended):
   To ensure Machine A is fully synchronized with any possible further changes (though unlikely immediately after a force push), you can also pull the latest changes from the remote repository on Machine A.

   ```sh
   cd ~/dotfiles
   git pull origin main
   ```

### Detailed Explanation

- **Force Push (`git push origin main --force`)**: This command will push your local changes to the remote repository, overwriting the remote branch with your local branch. This is useful when your local changes are intended to replace the remote state entirely.
- **Fetch (`git fetch origin`)**: This command will download objects and refs from another repository.
- **Reset (`git reset --hard origin/main`)**: This command will reset your local branch to match the state of the remote branch, discarding any local changes that are not in the remote branch.

---

### Maintenance - Regular Syncing to maintain consistency

By following these practices, both Machine A and Machine B will stay in sync with the remote repository and each other, minimizing the need for force pushes and hard resets.

#### On Either Machine (A or B)

1. **Pull Latest Changes Before Making Updates**

   ```sh
   cd ~/dotfiles
   git pull origin main
   ```

2. **Make Updates, Commit, and Push**:

   ```sh
   git add .
   git commit -m "Describe your changes"
   git push origin main
   ```

#### On the Other Machine (A or B)

3.**Pull Latest Changes to Sync**:

   ```sh
   cd ~/dotfiles
   git pull origin main
   ```

{{ page.path }}
