---

title: Quickstart - Multipass
description: Multipass is a Ubuntu Linux emulator you can run on MAC OS terminal
date: 2024-05-19 9:45:00 -0600
categories: [tools,virtualization]
tags: [cmd,linux,ubuntu,multipass]
image:
  path: /assets/images/covers/cover-multipass.png
  thumbnail: /assets/images/covers/cover-multipass.png
  alt: "Multipass"
media_subpath: /assets/images/

---
**What is Multipass ?**
It's a Ubuntu Linux emulator you can run on MAC OS terminal

### Install
- `brew install --cask multipass` - Install

### Launch
- `multipass launch` - Launch (random vm created)
- `Multipass launch --name <image name>` - Launch specific image
- `Multipass shell <vmname>` - run linux VM

### Info
- `multipass info <image name>` - Information about running instance
- ``Multipass find`` - show available images
- `Lsb_release -a` - Check ubuntu version

### Create a Multipass VM
```bash
multipass launch --cpus 2 --disk 10GB --mem 4G --name vm01
```

### Delete VM + Purge
```bash
multipass delete <vmname>
multipass purge
```

#### Links
[Multipass Instructions](https://multipass.run/docs/installing-on-macos)