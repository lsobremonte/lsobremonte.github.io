---
title: Terminal Apps
description: a list of mac OS terminal apps
date: 2024-05-11 09:35:00 -0600
categories: [apps]
tags: [cmd, macos, brew]
image:
  path: /assets/images/covers/cover-terminal-apps.png
  thumbnail: /assets/images/covers/cover-terminal-apps.png
  alt: "MacOS"
media_subpath: /assets/images/
---

**[Links]**
[Terminal Tools]({% link _posts/2024-05-16-terminal-tools.md %})

## Create Table of Contents

- [CLI Tools to try](#cli-tools-to-try)
- [HomeBrew Installer](#homebrew-installer)
- [Azure CLI](#azure-cli)
- [Python](#python)
- [Docker](#docker)
- [TerraForm](#terraform)
- [Github](#github)
- [PIP Package Installer](#pip-package-installer)
- [Speed Test](#speed-test)
- [PowerShell Upgrade](#powershell-upgrade)
- [Matrix Code](#matrix-code)
- [Busyness Fancy fake terminal](#busyness-fancy-fake-terminal)
- [NCDU Disk usage](#ncdu-disk-usage)
- [EZA Modern LS Tool](#eza-modern-ls-tool)
- [BAT Modern CAT Tool](#bat-modern-cat-tool)
- [FZF](#fzf)
- [Rip Grep Moder Grep tool](#rip-grep-moder-grep-tool)
- [ENTR](#entr)
- [Auto Suggestions](#auto-suggestions)
- [Neo Vim](#neo-vim)
- [TopGrade](#topgrade)

---

### CLI Tools to try

- [ ] [7 Amazing CLI Tools You Need To Try](https://www.youtube.com/watch?v=mmqDYw9C30I&list=WL&index=2&t=573s)
- [ ] Github Copilot command line
- [ ] Azure CLI

### HomeBrew Installer

description: Homebrew is a package manager for macOS that simplifies the installation of software on Apple's macOS operating system and Linux.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Azure CLI

description: Azure CLI is a command-line tool that provides a set of commands used to manage Azure resources.

```bash
brew update && brew install azure-cli
```

### Python

description: Python is a high-level, interpreted, and general-purpose programming language.

```bash
brew install python
```

### Docker

description: Docker is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers.

```bash
Brew install —cask docker
```

### TerraForm

description: Terraform is an open-source infrastructure as code software tool created by HashiCorp.

```bash
brew tap hashicorp/tap
brew install hashicorp/tap/terraform
```

### Github

description: GitHub is a web-based platform used for version control and collaboration.

```bash
brew install gh
```

### PIP Package Installer

description: pip is a package installer for Python.

```bash
sudo easy_install pip
```

### Speed Test

description: Speedtest-cli is a command-line interface for testing internet bandwidth using speedtest.net.

```bash
Brew install speedtest-cli 
```

### PowerShell Upgrade

description: PowerShell is a task automation and configuration management framework from Microsoft.

```bash
brew upgrade powershell --cask
```

### Matrix Code

description: Cmatrix is a simple command-line program that shows a scrolling 'Matrix' like screen in your terminal.

```bash
Brew install cmatrix
cmatrix
```

### Busyness

description: Hollywood is a fake terminal that emulates the look of a Hollywood hacking scene.

```bash
brew install hollywood
docker run --rm -it bcbcarl/hollywood
```

### NCDU

description: Ncdu is a disk usage analyzer with an ncurses interface.

```bash
Brew install NCDU
```

### EZA

description: Eza is a modern ls command with a more user-friendly output.

```bash
Brew install eza
```

### BAT

description: Bat is a modern cat command with syntax highlighting and Git integration.

```bash
# install
Brew install bat --install

# List Themes
bat --list-themes

# set Theme
export BAT_THEME="Coldark-Dark"

# Set theme permanently
echo 'export BAT_THEME="TwoDark"' >> ~/.bashrc
source ~/.zshrc #reload to apply changes

```

### FZF

description: Fzf is a command-line fuzzy finder that can be used with any list; files, command history, processes, hostnames, bookmarks, git commits, etc.

```bash
# Install
Brew install fzf

# Set up fzf key bindings and fuzzy completions for shell
[ -f ~/.fzf.zsh ] && source ~/.fzf.zsh
source ~/.zshrc
```

### RipGrep

description: Ripgrep is a line-oriented search tool that recursively searches your current directory for a regex pattern.

```bash
Brew install rg
```

### ENTR

description: Entr is a utility for running arbitrary commands when files change. It is
designed to run arbitrary commands whenever files change in a specified directory.

```bash
Brew install Entr
```

### Auto Suggestions

description: Zsh-autosuggestions is a zsh plugin that suggests commands as you type based on history and completions.

```bash
It suggests commands as you type based on history and completions.

```bash
brew install zsh-autosuggestions # Install
```

- Add plugin to ~/.zshrc (see below screenshot)

![Add plugin](/assets/images/content/example-add-plugin-zshrc.png)

### Neo Vim

description: NeoVim is a highly configurable text editor built to enable efficient text editing.

```bash
brew install nvim
```

### TopGrade

description: Topgrade is a command-line utility that upgrades all your installed packages.

```bash
brew install topgrade
```
