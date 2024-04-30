---
title: Git Commands
date: 2024-04-29 21:30:00 -0600
categories: [Command Line,DevOPs]
tags: [git,bash]
---

## Initialize a folder for Git
`git init <filename>` -- or `git init` to initialize the current folder
`rm -rf .git` -- or `rm -rf <filename>` to remove initialized git folder

## Add files to repo
* `git add <filename>` --add a single file
* `git add .` --add all files

## Move file back from Staging Area
* `git restore --staged <filename>`--unstage a single file
* `git restore --staged .` to unstage all files

## Snapshot restore
* `git reset <commit #>`--reset to a specific commit

## Git Commit
* `git commit -m "type message here"` --commit with a message

## View Commit history
* `git log` --view commit history
* `git log --pretty=oneline` --view commit history in one line
* `git patch` --view commit history in patch format
* `git show <commit#>` --show a specific commit

## Clone GIT Repo
* `git clone https://github.com/libgit2/libgit2` --clone a repo

## Upload local repo to "main" branch
* `git push origin main` --push to main branch

## Git Fetch local to cloud differences
* `git fetch` --fetch updates

## Git Pull
* `git pull` --pull changes from the cloud

## SSH into GitHub
* `ssh -T git@github.com` --SSH into GitHub

## Rename or Delete using Git
* `git mv file file2` --rename a file
* `git rm file` --remove a file
