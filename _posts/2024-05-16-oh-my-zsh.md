---

title: Oh-My-ZSH Setup
description: setup Oh-My-ZSH with themes and plugins
date: 2024-05-16 08:17:00 -0600
categories: [customization]
tags: [cmd, macos,iterm2,oh-my-zsh]
image:
  path: /assets/images/covers/cover-oh-my-zsh.png
  thumbnail: /assets/images/covers/cover-oh-my-zsh.png
  alt: "Oh-My-ZSH"
media_subpath: /assets/images/
---

# Oh-My-ZSH Setup
This customizes the terminal with themes and plugins

-----------------------------------------------
### 1. Install Iterm2

### 2. [Install Oh-My-ZSH](https://gist.github.com/n1snt/454b879b8f0b7995740ae04c5fb5b7df)
```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
* homebrew version available ?

### 3. [Install Powerline Fonts](https://github.com/powerline/fonts)

### 4. Set the font in Iterm2
Preference > Profiles > Text > Font
ie. Roboto Mono for Powerline

### 5. Set Iterm2 theme:
- solarized dark
- Theme to "Minimal"
- Text to Bold + 14 font size

### 6. Edit ~/.zshrc for [Agnoster ZSH Theme](https://github.com/agnoster/agnoster-zsh-theme)
```bash
ZSH_THEME="agnoster"
```
• Note: in the video he uses "bullet-train"

### 7. Update install (home directory)
```bash
Source ~/.zshrc
```

### 9. [Install fancy APPLE symbol and config info show (optional)**](https://github.com/dylanaraps/neofetch/wiki/Installation)
- Run the Latest Git Master (Bleeding Edge) instructions

### 10. [Install iterm2-monokai-pro](https://github.com/ayatmaulana/iterm2-monokai-pro)


