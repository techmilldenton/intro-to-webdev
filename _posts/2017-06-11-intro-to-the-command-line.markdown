---
layout: post
title: "Intro to the Command Line"
tags: 
date: 2017-06-11T00:53:30-05:00
---
One of the first tools any new web developer must become comfortable with is the command line. No matter which language you program in, you'll use the command line constantly. In this lesson we'll walk through what the command line is, what it looks like, and how to access it. In the next lesson we'll learn how to interact with the command line by executing commands. Let's get started!

## Graphical User Interface

We often access computer programs through their **Graphical User Interface** or **GUI**, for short . This is simply the visual and/or graphic component of a computer program.

For instance, word processing software generally offers a GUI with whitespace for us to type in, a cursor to indicate where we're typing, and a variety of buttons, menus, and options to format our work. This is a GUI. It's the visual portion of a program that we see, and interact with.

An email inbox that displays each email's details, allows us to open an email by clicking on it, and offers buttons to reply and format text is another example of a GUI.

## The Terminal

However, when we are developing we often use our computer's terminal interface. The **terminal** is a text-based interface that allows a user to interact with the computer by entering commands on a **command line**.

You have probably navigated through the folders and files on your device using a GUI tool such as _Finder_ on a Mac or _Explore_ on Windows. In the next lesson we'll explore how to create, update, delete and navigate folders and files using the terminal. We'll also see how the terminal provides access to additional commands not available through a GUI.

In summary, a graphical user interface (GUI) allows users to interact with a computer through menus, buttons, and other options we can see on the screen. The terminal, on the other hand, allows us to interact with a computer by typing text-only commands directly into the command line.

### Accessing the Terminal

So, we know the command line allows us to type text commands directly to our computer. And the terminal is the program through which we access the command line. In this section, we'll walk through how to access your Terminal program and the command line it contains.

#### Mac Setup

On a Mac, the Terminal application is located in the _Utilities_ folder, which is located inside the _Applications_ folder. You may also locate the Terminal by clicking the magnifying glass icon at the upper right corner of the screen and typing _"Terminal"_. Go ahead and do this now.

#### Windows Setup

Windows uses a Terminal program as well, but a Terminal with all the capabilities we'll require is not installed by default. Thankfully, we can easily download and install a Terminal program that does fit our needs.

There are many options available, but we recommend using a terminal program called **git bash**. You can download this free program at [msysgit.github.io](https://git-for-windows.github.io/). Go ahead and do this now.

### The Prompt

When you first open the terminal, you should see a short snippet of text followed by a grey or blinking rectangle. This rectangle is your cursor. Where the cursor is located is the command line itself, where we will type and execute commands.

The snippet of text left of the cursor is the command line **prompt**. This prompt contains some brief contextual information, such as the user account you're currently logged into the computer with, and your current location.

    techmill-5:~ Guest$ 

In the example above:

*   `techmill-5` is the nickname of the computer we're using.

*   `~` denotes that our current location is the home directory.

*   `Guest` informs us we're logged into an account named `Guest`.

*   This is all followed by a dollar sign `$`. This symbol denotes the end of the prompt and the beginning of the command line.

Also, not all prompts look the exact same. Depending on the nickname of your machine, and the name of your user account, your own command line prompt will differ. So don't worry if yours appears different from the example above; that's completely normal.

### Command Line Command Notation

When command line commands are written; whether here in our curriculum, or in other resources throughout the web, they are often preceded by a `$`.

This simply means the command is meant to be executed in the command line. The dollar sign is the common notation to communicate this because, as we just learned, most terminals display a dollar sign `$` at the end of the prompt, right before the command line.

When you see this symbol preceding a command, know that you are not required to _literally type_ a dollar sign into the command line. You will only type the command listed _after_ the dollar sign. The dollar sign simply denotes that the command is meant to be executed in the command line.

Great! Now that we understand the basics of the terminal and command line, let's begin practicing commands. In the next lesson we'll learn about the most frequently-used commands, how and when to execute them, and what they allow us to do.