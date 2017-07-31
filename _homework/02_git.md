---
layout: post
title: "02 - Git"
icon: git
---

## 1. Setting up a Git project
****
### Terminology
* **initialize:** In Git, to create a new, empty repository to track changes to the project directory. Created in the project directory
* **global:** A configuration option that refers to every directory in every location of the device
* **hidden files:** Are not listed with an ls terminal command, but will be displayed with an ls -a terminal command. The .git directory is hidden by default.

### Git Workflow
Be sure to set your global user information (name and email) if you haven't yet. You only need to do this once
```
$ git config --global user.name "Padma Patil"
$ git config --global user.email padma@email.com
```

## Create a new project directory with Git repository
In your terminal:
```
$ cd Desktop
$ mkdir hello-world
$ cd hello-world
$ git init
```
_What is happening at each step?_

## 2. Tracking changes with Git
****
### Add file(s) to track in Git
```
$ git add hello-world.html
```
or if multiple files should be added the . can be used to add all files:
```
$ git add .
```
### Commit
```
$ git commit -m "add a short, descriptive present tense commit message here describing the changes made"
```
### Git Commands
In this reference, examples in brackets `[xxx]`, should be entirely replaced by what is indicated (do not leave brackets).

#### Set up configurations
* `git config --global user.name "[name]"` - sets a SINGLE user name for all commits.
* `git config --global user.email "[email address]"` - sets a SINGLE email for all commits.

#### Committing
* `git add .` - Adds ALL files with changes to be committed.
* `git add [file]` - Adds the named file to be committed.
* `git commit -m "[message]"` - Records all of the staged files permanently to the version history; message should describe the changes finishing the phrase "This commit will…".

  Example:
  `git commit -m "add AJAX functionality to the comments form"`

#### Reviewing Git Information
* `git log` - Lists commit history for the current branch.
* `git status` - Lists the files where changes have been made to be committed.

## 3. Git-It workshop
****
For anyone who wants more practice and understanding of Git, I would recommend you run through the Git-It workshop. This will take you through creating repos, making branches, and even submitting pull requests. Check it out!

#### [Git-It workshop on GitHub](https://github.com/jlord/git-it-electron)