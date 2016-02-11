---
title: Notes on Git
author: John Williams
---

# Overview

These are some brief notes for me to help me learn Git.  Here is what
I want to do, and the relevant commands for doing so:

1. Add an existing local directory to Github
    1. Upload snapshots
    1. Get a list/description of snapshots (**git branch**)
    1. Revert to a specific branch

2. Contribute to an existing project
    1. Clone a project
	1. Make a change and upload it
	1. Notify the owner that the change is available

## Set up Git for the first time


1. **git config --global user.email** <email address>
1. **git config --global user.name** <name>
1. **git config --global core.editor emacsclient -nw** 

## Working with remotes

1. **git remote add** <short name> <URI>, e.g. GH https://github.com/johnfrombluff/master
1  **git remote -v**
1. **git fetch GH**


## Workflow for an established directory/local repository

### Sync changed files

1. **git add** <files>
1. **git commit -m** <message describing changes>
1. **git push**

Does this imply that the **.git** directory below the top-level directory
contains information about the remote URI?

### Remove files from the repository

1. **git rm** <file> removes the file from remote *and* local
1. **git rm --cached** <file> only removes it from the remote


# Branching

## Overview

- Create a branch: **git branch** <name>
- List branches:  **git branch**
- Switch branches: **git checkout**

## Create a branch
- **git branch** <branch name>

## Make changes part of a "branch"

Make sure your local repository is synced, then create branch.

1. **git pull**
1. **git checkout -b** <new branch name>
1. **git push origin** <new branch name>
1. **git push --set-upstream origin** <W2S-Panter>

# Open questions

## Why do you have to add and commit separately?
I'm not sure, but I think it's because Git has a notion of *staging* a
**set** of changes prior to comitting them. So each file (or even part
of a file?) can be **add**ed to the staging set, and then all the
stage changes are **committ**ed.

## What is the workflow for contributing to an existing project?

Is it: 

1. Git clone
1. Create a branch
1. Make changes
1. Commit them
1. Sync them with a remote repository
1. Alert the maintainer that the changes are there? ("Send a pull request"?)


