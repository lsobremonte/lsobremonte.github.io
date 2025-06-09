---
title: Terminal Commands
description: Useful Terminal Commands
date: 2024-05-16 16:00:00 -0600
categories:
  - CMD

tags: [iterm2, cmd, terminal]
image:
  path: assets/images/covers/cover-terminal-commands.png
  thumbnail: assets/images/covers/cover-terminal-commands.png
  alt: "Terminal Commands"
media_subpath: /assets/images/
---

**[Links]**
[Terminal Apps]({% link _posts/2024-05-11-terminal-apps.md %})

<h1 style="text-align: center;"> Terminal Commands </h1>

![Add plugin](/assets/images/content/terminal-icon.png)

## Table of Contents

- [Copy](#copy)
- [Delete](#delete)
- [Search and Find](#search-and-find)
- [Compare](#compare)
- [FZF](#fzf)
- [Networking](#networking)

---

<h2 id="copy">Copy</h2>
<details open>
<summary>Copy Commands</summary>

<div markdown="1">

### Copy All Files

```bash
rsync -avh --delete SOURCE="/Volumes/SourceDrive/" DEST="/Volumes/DestinationDrive/"
```

### Copy iCloud Files

```bash
rsync -av --update ~/Library/Mobile\ Documents/com~apple~CloudDocs/ /Volumes/ExternalDrive/Backup/
```

### Copy Files from Remote Mac

```bash
rsync -avz -e ssh user@mac1.local:"/source/path/" "/destination/path/"
```

</div>

</details>

---

<h2 id="delete">Delete</h2>
<details>
<summary>Delete Commands</summary>

<div markdown="1">

### Delete Files with Word "python" and Confirm

```bash
find . -type f -name '*python*' -exec rm -i {} \;
```

### Delete All Files Within Current Folder

```bash
rm -rf *
```

### Delete Empty Folder That Ends with a 2

```bash
find . -type d -name '*2' -empty -delete
```

### Delete All Files Including Hidden Files

```bash
find . -mindepth 1 -delete
```

</div>

</details>

---

<h2 id="search-and-find">Search and Find</h2>
<details>
<summary>Search and Find Commands</summary>

<div markdown="1">

### List Full Path for File

```bash
readlink -f filename
```

### Find All .py Files

```bash
find . -type f -name "*.py"
```

### Search for a String

```bash
find . -type f -exec grep --color=always -H "<string>" {} \;
```

### Find Latest Ubuntu Version in Azure

```bash
az vm image list --offer UbuntuServer --publisher Canonical --sku 18.04-LTS --all --output table
```

</div>

</details>

---

<h2 id="compare">Compare</h2>
<details>
<summary>Compare Commands</summary>

<div markdown="1">

### Compare File Trees

```bash
rsync -an --out-format="%M %f" file01.old/ file01.new/
```

</div>

</details>

---

<h2 id="fzf">FZF</h2>
<details>
<summary>FZF Commands</summary>

<div markdown="1">

### Preview with bat

```bash
fzf --preview="bat --color=always {}"
```

### Save Command Line History in ZSH

```bash
source <(fzf --zsh)
HISTFILE=~/.zsh_history
HISTSIZE=10000
SAVEHIST=10000
setopt appendhistory
source .zshrc
```

### Find Folder via FZF

```bash
cd "$(find . -type d | fzf)"
```

</div>

</details>

---

<h2 id="networking">Networking</h2>
<details>
<summary>Networking Commands</summary>

<div markdown="1">

### Scan Network

```bash
nmap -sn 192.168.0.1/24
```

### Check for Open Ports

```bash
nmap <computer>
```

### Output SSL Certificates for a Host

```bash
nmap --script ssl-cert -p 443 <url>
```

### Show Supported TLS and Ciphers

```bash
nmap --script ssl-enum-cipher -p 443 git.home.creative.de
```

### Packet Analyzer with tcpdump

```bash
tcpdump -i en0
tcpdump -i $INTERFACE
tcpdump -i $PORT
# Didn't work on mac:
tcpdump -i 443
```

### Capture Packets for Wireshark

```bash
sudo tcpdump -i en0 port 443 and host 192.168.0.217 -w test.pcap
```

### Network Performance Testing with iperf

#### Listening

```bash
iperf -s -p $PORT
iperf -s -p 6700
```

#### Connecting

```bash
iperf -c 192.168.0.217 -p 6700
```

</div>

</details>
