---

title: Quickstart - Stow
description: This directory contains the dotfiles for my system
date: 2024-05-04 21:30:00 -0600
categories: [cmd,devops,backups,linux]
tags: [git,bash,stow]
image:
  path: /assets/images/covers/cover-dotfiles.png
  thumbnail: /assets/images/covers/cover-dotfiles.png
  alt: "Stow"

---

 ## Overview

`GNU Stow` helps you backup your Dotfiles (configuration files). So when you "stow" a file, it will create a `symlink` between your file and an identical file in our home directory.

---

## Installation

```bash
brew list git # check if git is installed
brew list stow # check if stow is installed
cd ~
mkdir dotfiles # Create a directory to store dotfiles

```



---

## Usage

### Add a dotfile
This works for both hidden file and folder

```bash
cd ~/dotfiles
mkdir ~/dotfiles/zsh # create folder
mv ~/.zshrc ~/dotfiles/zsh # move dotfile into dotfile folder
stow zsh # create a symlink
ls -ld ~/.zshrc # check for new symlink
```

### GIT version Control
```bash
git add .
git commit -m "Manage nvim config with stow"
git push # upload local repository content to remote repository
```

### Restore folders from git (untested)

This shows how to restore folders from git using stow on a fresh machine

```bash
git clone your-repository-url ~/dotfiles # download
cd ~/dotfiles
stow folder-name  # Replace 'folder-name' with the name of the folder containing your config files, e.g., zsh, oh-my-zsh, etc.
```

### Clean up Symlinks from home directory (untested)
```bash
stow -D folder-name # Remove symlink
```




---

## List of hidden User configuration files for stow backup and restore

* `.zshrc `- Zsh configurations (file).
* `.oh-my-zsh` - Configuration for Oh My Zsh (directory).
* `.gitconfig` - Global Git configuration settings (file).
*  `.vimrc` - Configuration for Vim (file).
