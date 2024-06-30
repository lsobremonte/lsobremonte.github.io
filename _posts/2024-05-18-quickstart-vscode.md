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

## Legend
- **Shift**: ⇧
- **Control** : ⌃
- **Option**: ⌥
- **Command**: ⌘

## Shortcuts

### Most Useful
- `⇧ + ⌘ + p` - Open the Command Palette
- `⌘ + p` : quick open menu
- `⌘ + ⇧ + k` - Remove line
- `~ + ⌃` - show/hide terminal
- `⌘ + b` : use for the show files
- `⌘ + /` - comment code
- ``⌘ + w`` - close file

### Connect to Azure Cloud Shell
- `⌘ + ⇧ + p` > "Open PowerShell in Cloud Shell"
- is this better than connect through terminal?

### Run Commands
- `fn + f8` - run PowerShell code
- `⌘ + ' `- run Bash code
- `⇧ + enter `- run Python (highlight code)


### Untested
- `click + ⌃ + f2` - multi select cursor
- `⇧ + ⌥ + f` - code formatting
- `⌃ + b` : scroll up and down
- `⌃ + \`: use for split editor window. 
- `⌃ +  ⇧ + v` - Open Markdown Preview
- `⌃ + k v` - Open Markdown Preview to the Side
- `⌃ + ⇧ + l` : use select all matches and then edit or del.
- `⌃+ D` : use for add selection to matches.
- `⌃ + ⌥ + down` : use for the duplicates lines


## Configuration

### Setup VSCode as default editor
- `Git config --global core.editor "code --wait --new-window"`

### Configure VSCode to launch from terminal
1. Open VSCode and press `⌘ + ⇧ + p` 
2. type and choose : Shell Command:install code command in PATH

### Edit User Settings (Mac OS)
- `⌘ + ⇧ + p` then type `settings.json`


### Select Python Interpreter (Virtual environment)
- `⌘ + ⇧ + p` > Select Python Interpreter 
- choose venv/bin/python or venv/bin/python3

### Set VSCode as GIT editor
1. Open the Command Palette (⇧⌘P)
2. type 'shell command' to find the Shell Command: `Install 'code' command in PATH command`.
3. Then try setting core editor with this command:
`git config --global core.editor "code --wait"`
