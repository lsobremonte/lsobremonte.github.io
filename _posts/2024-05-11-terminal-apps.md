---
title: Terminal Apps
description: a list of mac OS terminal apps
date: 2024-05-11 09:35:00 -0600
categories: [Apps, Command-tool]
tags: [macos, brew, cmd]
image:
  path: /assets/images/covers/cover-terminal-apps.png
  thumbnail: /assets/images/covers/cover-terminal-apps.png
  alt: "MacOS"
media_subpath: /assets/images/
---

**[Links]**
[Terminal Tools]({% link _posts/2024-05-16-terminal-tools.md %})

## Create Table of Contents

- [HomeBrew](#homebrew-installer)
- [FZF](#fzf)
- [BAT](#bat)
- [EZA](#eza)
- [RipGrep](#ripgrep)
- [Zoxide](#zoxide)
- [ZSH-Auto Suggestions](#zsh-auto-suggestions)
- [ENTR](#entr)
- [Docker](#docker)
- [Lazy Docker](#lazy-docker)
- [OrbStack](#orbstack)
- [Github](#github)
- [Lazy Git](#lazy-git)
- [Neo Vim](#neo-vim)
- [Python](#python)
- [PIP](#pip)
- [Azure CLI](#azure-cli)
- [TerraForm](#terraform)
- [TopGrade](#topgrade)
- [NCDU](#ncdu)
- [Speed Test](#speed-test)
- [PowerShell Upgrade](#powershell-upgrade)
- [Nmap](#nmap)
- [Glow](#glow)
- [Matrix Code](#matrix-code)
- [Busyness](#busyness)

---

### HomeBrew Installer

**Package manager for macOS** that simplifies the installation of software on Apple's macOS operating system and Linux.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
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

### EZA

**Modern LS** command with a more user-friendly output.

```bash
Brew install eza
```

### RipGrep

Line-oriented search tool that **recursively searches** your current directory for a **regex pattern**.

```bash
Brew install rg
```

### Zoxide

A smarter **cd command** that learns your habits and provides quick directory navigation.

```bash
brew install zoxide

# Add to your shell config (~/.zshrc or ~/.bashrc)
eval "$(zoxide init zsh)"

# Basic usage
z foo    # Jump to a directory containing "foo"
zi       # Interactive selection
```

### ZSH-Auto Suggestions

Plugin that **suggests commands** as you type based on history and completions.

```bash
brew install zsh-autosuggestions # Install
```

- Add plugin to ~/.zshrc (see below screenshot)

![Add plugin](/assets/images/content/example-add-plugin-zshrc.png)

### ENTR

Utility for **running arbitrary commands when files change**. It is designed to run arbitrary commands whenever files change in a specified directory.

```bash
Brew install Entr
```

### Docker

Set of platform as a service products that use **OS-level virtualization** to deliver software in packages called **containers**.

```bash
Brew install —cask docker
```

### Lazy Docker

A simple terminal UI for both **docker** and **docker-compose**, written in Go with the gocui library.

```bash
brew install lazy-docker

# Basic usage
lazydocker  # Launch the UI
# Use arrow keys to navigate
# Press 'd' to view containers
# Press 'i' to view images
```

### OrbStack

A fast, light, and simple **Docker** & **Kubernetes** development environment for macOS.

```bash
brew install orbstack

# Basic usage
orb start        # Start OrbStack
orb status       # Check status
orb shell        # Open shell in default container
```

### Github

Web-based platform used for **version control** and collaboration.

```bash
brew install gh
```

### Lazy Git

Simple terminal UI for **git** commands, written in Go with the gocui library.

```bash
brew install lazygit

# Basic usage
lazygit  # Launch the UI
# Use arrow keys to navigate
# Press 'space' to stage/unstage files
# Press 'c' to commit
```

### Neo Vim

Highly configurable **text editor** built to enable efficient text editing.

```bash
brew install nvim
```

### Python

High-level, interpreted, and general-purpose **programming language**.

```bash
brew install python
```

### PIP

**Package installer** for Python.

```bash
sudo easy_install pip
```

### Azure CLI

Command-line tool that provides a set of commands used to **manage Azure resources**.

```bash
brew update && brew install azure-cli
```

### TerraForm

Open-source**infrastructure as code** software tool created by HashiCorp.

```bash
brew tap hashicorp/tap
brew install hashicorp/tap/terraform
```

### TopGrade

Command-line utility that **upgrades** all your installed packages.

```bash
brew install topgrade
topgrade
```

### NCDU

**Disk usage** analyzer with an ncurses interface.

```bash
Brew install NCDU
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

### Nmap

Network exploration and security auditing tool that **scans networks** for open ports, running services, and live hosts.

```bash
brew install nmap

# Basic usage
nmap localhost              # Scan localhost
nmap 192.168.1.0/24        # Scan entire subnet
nmap -p 80,443 example.com # Scan specific ports
```

### Glow

Terminal based **Markdown** renderer designed to work well with CLI tooling.

```bash
brew install glow

# Basic usage
glow README.md           # View a markdown file
glow -p .               # View all markdown files in current directory
glow -s dark README.md  # Use dark theme
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
