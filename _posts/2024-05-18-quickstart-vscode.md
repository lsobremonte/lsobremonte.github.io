---

title: Quickstart - VS Code
description: VS Code quickstart guide
date: 2024-05-18 6:40:00 -0600
categories: [tools,coding]
tags: [vscode,python,shortcuts]
image:
  path: /assets/images/covers/cover-vscode.png
  thumbnail: /assets/images/covers/cover-vscode.png
  alt: "VS Code"
media_subpath: /assets/images/

---

## Shortcuts

### Most Useful
- `cmd + p` : quick open menu.
- `cmd + shift + k` - Remove line
-  `~ + ctrl` - show/hide terminal
- `cmd + b` : use for the show files.
- `cmd + /` - comment code
- ``cmd + w`` - close file.

### Connect to Azure Cloud Shell
- `CMD + Shift + P` > "Open PowerShell in Cloud Shell"
- is this better than connect through terminal?

### Run Commands
- `fn + f8` - run PowerShell code
- `command + ' `- run Bash code
- `shift + enter `- run Python (highlight code)


### Untested
- `click + ctrl + f2` - multi select cursor
- `shift + alt + f` - code formatting
- `ctrl + b` : scroll up and down
- `ctrl + \`: use for split editor window. 
- `ctrl +  Shift + v` - Open Markdown Preview
- `ctrl + k v` - Open Markdown Preview to the Side
- `ctrl + shift + l` : use select all matches and then edit or del.
- `ctrl+ D` : use for add selection to matches.
- `ctrl + alt + down` : use for the duplicates lines



## Configuration
### Setup VSCode as default editor
- `Git config --global core.editor "code --wait --new-window"`

### Configure VSCode to launch from terminal
1. Open VSCode and press `cmd + shift + p` 
2. type and choose : Shell Command:install code command in PATH

### Edit User Settings (Mac OS)
- `Cmd + Shift + P` then type `settings.json`

### Select Python Interpreter (Virtual environment)
- `cmd + shift + p` > Select Python Interpreter 
- choose venv/bin/python or venv/bin/python3

### Set VSCode as GIT editor
1. Launch VS Code. 
2. Open the Command Palette (⇧⌘P)
3. type 'shell command' to find the Shell Command: `Install 'code' command in PATH command`.
4. Then try setting core editor with this command:
`git config --global core.editor "code --wait"`