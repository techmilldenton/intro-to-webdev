---
layout: post
title: "Git & Github"
tags: 
date: 2017-07-13T18:01:38-05:00
---
---
layout: post
title: "Git & Github"
tags: 
date: 2017-07-13T18:01:38-05:00
---
When we get started writing a new program, the last thing we want to happen is to lose any of our hard work. To prevent this from happening, we will save versions of our code on our computer AND also save a version of our code on a location on the web. We will learn to manage these different versions of our code using two tools: **Git** and **GitHub**.

### Git
Git is a **version control system** that we install on the computers where we write code. Git allows us take a snapshot of our program, called a **commit**, at important points along the way as we work.

You can think of a commit like a save point on a document that you are writing. Although unlike a save, once a commit is made, it is permanently stored in the history of the project. A newer commit does not overwrite the previous commit. If we ever want to go back to the place in time where the commit was made, where all the files looked exactly as they did when we committed, we will be able to do so.

>_You can think of a commit like a save point on a document that you are writing._

Additionally, commits are made with brief messages that describe the changes/additions being saved. For instance, if we were creating a basic website, and added a contact page with our email and phone number, when we saved those changes by committing we would include a message like _"Add contact page with email and phone number."_

Commit messages are written in present tense (ie: _"Add contact page..."_ not _"Added contact page..."_).

### GitHub
When we are ready to save the code from our computers to a location on the web, we will use [GitHub](https://github.com). GitHub allows us to create **repositories** to store the code and code history for each of our projects. A repository is what we call the container that holds all of the files from our project with all of the commits that have been made to it. GitHub is designed to work seamlessly with Git.

Each project that we create will be saved to a repository on GitHub. By the end of your time here, you will have a portfolio of your work represented by all of your GitHub repositories. LinkedIn will be your employment resume and GitHub will serve as your coding resume.

Do note that all repositories on GitHub are public by default. For a monthly fee, GitHub does offer [unlimited private repositories](https://github.com/blog/2164-introducing-unlimited-private-repositories). However, this is entirely optional. Private repos are not required for this course. It's standard practice for most developers to simply leave everything public, even if projects are still a work in progress.

We'll walk through exactly how to use both Git and GitHub in an upcoming lesson. For now, simply remember that Git is the tool we'll use to save all changes and additions to our code on the computer we're working on. GitHub is the online location we can upload our Git-managed code to for safekeeping.

### Installing Git on Macs
To install Git on your personal Mac, follow these steps:

First, go to the terminal and copy and paste this code at the prompt:

```$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```

This installs the package manager, Homebrew, on your device. It may take a moment for Homebrew to download and install. This is perfectly normal. Depending on your machine's configuration, you may also be prompted to enter the password for your user account.

Next, we add this so that Homebrew packages are run before the system versions of the same (which may be dated or not what we want):

```$ echo 'export PATH=/usr/local/bin:$PATH' >> ~/.bash_profile```

Last, install Git with this command:

```$ brew install git```
Done!

### Installing Git on Windows
After installing git bash on your Windows machine, as instructed in the Introduction to the Command Line lesson, Git should be ready to use within your git bash program.

### Creating a GitHub Account
If you have not already created a personal GitHub account to store your code, head over to the GitHub website and sign up for a free account now.

When creating an account, consider choosing a username that you will feel comfortable sharing in a professional setting. Also, keep in mind that all of the work that you will be adding to your GitHub account is viewable to the public. Make a commitment to always present the best version of your code. Again, your Github profile will serve as your resume and portfolio of coding abilities.