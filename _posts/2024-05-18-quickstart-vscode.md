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

### Configure VSCode to launch from terminal
Open Visual Studio Code and press Command + Shift + P or F1 then type Shell in command palette now you are able to find this option like Shell Command : Install code in PATH

- `Git config --global core.editor "code --wait --new-window"` - Setup VSCode as default editor


### User Settings (Mac OS)

`Cmd + Shift + P`
• Type settings.json

### Python Interpreter (Virtual environment)

- `cmd + shift + p` > Select Python Interpreter 
- choose venv/bin/python or venv/bin/python3

### Shortcuts

- `CTRL+ B` : use for the show files.
- `CTRL + ~` : use for the open and closed terminal.
- ``CTRL  + P`` : use for the quick open menu.
- ``CTRL + B ``: scroll up and down (Doesn't work)
- ``CTRL + \`` : use for split editor window.  (Doesn't Work)
- ``CTRL + W`` : use for the closed file.
- ``CTRL + shift + l`` : use select all matches and then edit or del.
- ``CTRL+ D ``: use for add selection to matches.
- ``CTRL + alt + down`` : use for the duplicates lines

### Most Useful

- `CTRL + Shift + K` - Remove line
- ` tick + ctrl` - hide terminal
- `Cmd + /` - comment code
- `Shift + Alt + F` - code formatting
- `Click + CTRL + F2` - multi select cursor

### Run Commands

- `fn + f8` - run PowerShell code
- `command + ' `- run Bash code
- `shift + enter `- run Python (highlight code)

### From VS Code Connect to Azure Cloud Shell

- `CMD + Shift + P` >  "Open PowerShell in Cloud Shell"

### Markdown Preview
- `Ctrl +  Shift + V` - Open Markdown Preview
- `Ctrl + K V` - Open Markdown Preview to the Side

### Set VSCode as GIT editor
- Launch VS Code. 
- Open the Command Palette (⇧⌘P)
- type 'shell command' to find the Shell Command: `Install 'code' command in PATH command`.
- Then try setting core editor with this command:
`git config --global core.editor "code --wait"`
