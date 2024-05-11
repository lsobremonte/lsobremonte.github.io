 ## Overview

`GNU Stow` helps you backup your Dotfiles (configuration files). So when you "stow" a file, it will create a `symlink` between your file and an identical file in our home directory.

---
## Installation

Ensure you have both Git and Stow installed first
- `brew list git` -- check if git is installed
- `brew list stow` -- check if stow is installed


```bash
brew list git # check if git is installed
brew list stow # check if stow is installed
cd ~
mkdir dotfiles # Create a directory to store dotfiles

```
![StowFlowchart](/assets/GNU-Stow-flowchart.png)


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


---

## List of hidden User configuration files for stow backup and restore

* `.zshrc `- Zsh configurations (file).
* `.oh-my-zsh` - Configuration for Oh My Zsh (directory).
* `.gitconfig` - Global Git configuration settings (file).
*  `.vimrc` - Configuration for Vim (file).
