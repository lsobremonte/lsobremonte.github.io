---

title: Iterm2 Terminal Customization
description:  Iterm2 terminal customizations
date: 2024-05-13 19:01:00 -0600
categories: [customization]
tags: [cmd, macos,iterm2,oh-my-zsh]
image:
  path: /assets/images/covers/cover-binarycode.png
  thumbnail: /assets/images/covers/cover-binarycode.png
  alt:  "Iterm2"
media_subpath: /images/content/
---

# Oh-My-ZSH Setup
This customizes the terminal with themes and plugins

-----------------------------------------------
**1. Install Iterm2**

**2. [Install Oh-My-ZSH](https://gist.github.com/n1snt/454b879b8f0b7995740ae04c5fb5b7df)
```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
* homebrew version available ?

**3. [Install Powerline Fonts](https://github.com/powerline/fonts)

**4. Set the font in Iterm2**
Preference > Profiles > Text > Font
ie. Roboto Mono for Powerline

**5. Set Iterm2 theme:**
- solarized dark
- Theme to "Minimal"
- Text to Bold + 14 font size

**6. Edit ~/.zshrc** for [Agnoster ZSH Theme](https://github.com/agnoster/agnoster-zsh-theme)
```bash
ZSH_THEME="agnoster"
```
• Note: in the video he uses "bullet-train"

**7. Update install (home directory)**
```bash
Source ~/.zshrc
```

**9. [Install fancy APPLE symbol and config info show (optional)**](https://github.com/dylanaraps/neofetch/wiki/Installation)
- Run the Latest Git Master (Bleeding Edge) instructions

**10. [Install iterm2-monokai-pro](https://github.com/ayatmaulana/iterm2-monokai-pro)



# Extra iTerm2 Configurations


### Set Iterm as Default Terminal
iTerm2 > Make iTerm2 Default Term

### Set Paste with Right-Click
![iterm2 preference](iterm2.preferences.png)

### Disable iTerm Password Manager
- Go to Advanced. 
- Type "animation" into search box. 
- Set "Disable animations for showing/hiding password manager" to Yes. Quit iTerm2

### iTerm2 Color Themes
[iTerm2 Color Themes](https://iterm2colorschemes.com/)

### HowTo - Set Iterm back to Default Settings
```bash
cd ~/Library/Preferences/
```
- defaults delete com.googlecode.iterm2

### Uninstall Powerlevel10k
![Uninstall Powerlevel10k](uninstall.powerlevel10k.png)

## Troubleshooting
### Issue - Why does my terminal have question marks ?

Explanation:   Insecure folder error 
[Zsh detects insecure completion-dependent directories](https://stackoverflow.com/questions/61433167/zsh-detects-insecure-completion-dependent-directories)
Fix:
```bash
chmod 755 /usr/local/share/zsh
chmod 755 /usr/local/share/zsh/site-functions
```


### Error - Insecure Folders
```bash
[oh-my-zsh] Insecure completion-dependent directories detected:
drwxrwxr-x  3 lsobremonte  admin   96 12 Dec  2020 /usr/local/share/zsh
drwxrwxr-x  5 lsobremonte  admin  160  7 Mar 21:37 /usr/local/share/zsh/site-functions
[oh-my-zsh] For safety, we will not load completions from these directories until
[oh-my-zsh] you fix their permissions and ownership and restart zsh.
[oh-my-zsh] See the above list for directories with group or other writability.
[oh-my-zsh] To fix your permissions you can do so by disabling
[oh-my-zsh] the write permission of "group" and "others" and making sure that the
[oh-my-zsh] owner of these directories is either root or your current user.
[oh-my-zsh] The following command may help:
[oh-my-zsh]     compaudit | xargs chmod g-w,o-w
[oh-my-zsh] If the above didn't help or you want to skip the verification of
[oh-my-zsh] insecure directories you can set the variable ZSH_DISABLE_COMPFIX to
[oh-my-zsh] "true" before oh-my-zsh is sourced in your zshrc file.
```


Fix:
[Zsh detects insecure completion-dependent directories](https://stackoverflow.com/questions/61433167/zsh-detects-insecure-completion-dependent-directories)



### Issue - Why does my VSCode terminal have different colours and bolded text which doesn’t match iterm2 colours ? 

FIX:
It’s because your VSCode setting 
```bash
"terminal.integrated.defaultProfile.osx": "zsh",
```
Is referencing your ./zshrc file and referencing
```bash
ZSH_THEME="agnoster"
```
Try a different theme like ‘robbyrussell’ (default oh my zsh theme).
