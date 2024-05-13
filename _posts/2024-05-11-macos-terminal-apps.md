---

title: MacOS Terminal Apps
description: a list of mac OS terminal apps
date: 2024-05-11 09:35:00 -0600
categories: [apps]
tags: [cmd, macos, brew]
image:
  path: /assets/images/covers/cover-terminal.png
  thumbnail: /assets/images/covers/cover-terminal.png
  alt: "Terminal Apps"

---

Overview:
Guide to all the cool terminal apps you can install on MacOS


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

---

### CLI Tools to try
- [ ] [7 Amazing CLI Tools You Need To Try](https://www.youtube.com/watch?v=mmqDYw9C30I&list=WL&index=2&t=573s)
- [ ] Github Copilot command line
- [ ] Azure CLI



### HomeBrew Installer
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Azure CLI
```bash
brew update && brew install azure-cli
```

### Python
```bash
brew install python
```

### Docker
```bash
Brew install —cask docker
```

### TerraForm
```bash
brew tap hashicorp/tap
brew install hashicorp/tap/terraform
```
### Github
```bash
brew install gh
```

### PIP Package Installer
```bash
sudo easy_install pip
```

### Speed Test
```bash
Brew install speedtest-cli 
```

### PowerShell Upgrade
```bash
brew upgrade powershell --cask
```

### Matrix Code
```bash
Brew install cmatrix
```

### Busyness Fancy fake terminal
```bash
# Run in docker
docker run --rm -it bcbcarl/hollywood
```


### NCDU Disk usage
```bash
Brew install NCDU
```


### EZA Modern LS Tool
```bash
Brew install eza
```

### BAT Modern CAT Tool
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
```bash
Brew install fzf
```


### Rip Grep Moder Grep tool
```bash
Brew install rg
```

### ENTR
designed to run arbitrary commands whenever files change in a specified directory.
```bash
Brew install Entr
```

### Auto Suggestions
[ZSH Autosuggestions)](https://github.com/zsh-users/zsh-autosuggestions)

```bash
brew install zsh-autosuggestions # Install
```

- `${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions` - Add plugin to ~/.zshrc file: plugins=(zsh-autosuggestions)


![Add plugin](/assets/images/content/example-add-plugin-zshrc.png)
