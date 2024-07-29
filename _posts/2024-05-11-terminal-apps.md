---
title: Terminal Apps
description: a list of mac OS terminal apps
date: 2024-05-11 09:35:00 -0600
categories: [Apps,Command-tool]
tags: [macos, brew,cmd]
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
- [Busyness](#busyness)
- [NCDU](#ncdu)
- [EZA](#eza)
- [BAT](#bat)
- [FZF](#fzf)
- [RipGrep](#ripgrep)
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

**Package manager for macOS** that simplifies the installation of software on Apple's macOS operating system and Linux.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Azure CLI

Command-line tool that provides a set of commands used to **manage Azure resources**.

```bash
brew update && brew install azure-cli
```

### Python

High-level, interpreted, and general-purpose **programming language**.

```bash
brew install python
```

### Docker

Set of platform as a service products that use **OS-level virtualization** to deliver software in packages called **containers**.

```bash
Brew install —cask docker
```

### TerraForm

Open-source**infrastructure as code** software tool created by HashiCorp.

```bash
brew tap hashicorp/tap
brew install hashicorp/tap/terraform
```

### Github

Web-based platform used for **version control** and collaboration.

```bash
brew install gh
```

### PIP Package Installer

**Package installer** for Python.

```bash
sudo easy_install pip
```

### Speed Test

Command-line interface for **testing internet bandwidth** using speedtest.net.

```bash
Brew install speedtest-cli 
```

### PowerShell Upgrade

Task **automation** and configuration management framework from Microsoft.

```bash
brew upgrade powershell --cask
```

### Matrix Code

Command-line program that shows a **scrolling 'Matrix'** like screen in your terminal.

```bash
Brew install cmatrix
cmatrix
```

### Busyness

**Fake terminal** that emulates the look of a Hollywood hacking scene.

```bash
brew install hollywood
docker run --rm -it bcbcarl/hollywood
```

### NCDU

**Disk usage** analyzer with an ncurses interface.

```bash
Brew install NCDU
```

### EZA

**Modern LS** command with a more user-friendly output.

```bash
Brew install eza
```

### BAT

**Modern CAT** command with syntax highlighting and Git integration.

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

Command-line fuzzy**finder** that can be used with any list; files, command history, processes, hostnames, bookmarks, git commits, etc.

```bash
# Install
Brew install fzf

# Set up fzf key bindings and fuzzy completions for shell
[ -f ~/.fzf.zsh ] && source ~/.fzf.zsh
source ~/.zshrc
```

### RipGrep

Line-oriented search tool that **recursively searches** your current directory for a **regex pattern**.

```bash
Brew install rg
```

### ENTR

Utility for **running arbitrary commands when files change**. It is
designed to run arbitrary commands whenever files change in a specified directory.

```bash
Brew install Entr
```

### Auto Suggestions

Plugin that **suggests commands** as you type based on history and completions.



```bash
brew install zsh-autosuggestions # Install
```

- Add plugin to ~/.zshrc (see below screenshot)

![Add plugin](/assets/images/content/example-add-plugin-zshrc.png)

### Neo Vim

Highly configurable **text editor** built to enable efficient text editing.

```bash
brew install nvim
```

### TopGrade

Command-line utility that **upgrades** all your installed packages.

```bash
brew install topgrade
```
