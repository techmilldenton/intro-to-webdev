---
layout: post
title: "Interacting With the Command Line"
tags: 
date: 2017-06-11T00:54:24-05:00
---
In the last lesson we learned about the terminal and its command line; including how to access and install it, and the notation commands are commonly conveyed in. Now, let's learn the specific commands we can execute to interact with our computer directly through the command line.

In this lesson we'll explore the most common commands executed through the command line. You'll use many of these _daily_ while at Epicodus. Let's get started!

## Basics

To enter a command we simply click within the terminal window and begin typing. Text will be inserted where our cursor is located, directly after the prompt. Then, after typing a command we can press enter to run it.

Let's look at some of these commands now.

### Retrieving Current Location with `<span class="pln">$ pwd</span>`

The `<span class="pln">$ pwd</span>` command prints your current location to the screen. `<span class="pln">pwd</span>` stands for _print working directory_.

Remember, similar to the Mac _Finder_ or Windows _Explore_ program, the command line allows us to look around our computer. We can navigate through folders and directories and see what's inside. The only difference is that _Finder_ and _Explore_ have graphical user interfaces, and the terminal does not.

So, by entering `<span class="pln">pwd</span>` into the command line and pressing enter, we can get our current location. It returns a file **path**, like this:

    epicodus-5:~ Guest$ pwd
    /Users/Guest

In the example above we typed `<span class="pln">pwd</span>` right after our command prompt. The terminal responded by printing out our current location for us. As you can see, we're located in the `<span class="typ">Users</span>` directory, in a folder called `<span class="typ">Guest</span>`.

When you open the Terminal application on a Mac, you will begin in your home directory. For example, if your username is Jesse, your home directory is _/Users/Jesse_. You can verify this by typing `<span class="pln">pwd</span>` at the command prompt and pressing Enter.

If you're navigating through files and folders in the command line and are unsure of your current location, you can always run the `<span class="pln">$ pwd</span>` command. It's like a _"You are here"_. Give this command a shot now.

### Listing All Content with `<span class="pln">$ ls</span>`

The `<span class="pln">$ ls</span>` command stands for _list_. Executing this command prompts the terminal to list out the directories (directories is just a technical term for folders) and files in our current location. Running this command looks something like this:

    epicodus-5:~ Guest$ ls
    Documents       Library         Pictures
    Applications        Downloads       Movies
    Desktop             Music           Public          

We can also list out the directories _inside_ of one of these directories by including its name after the `<span class="pln">$ ls</span>` command. The command and specific directory name should be separated by a space.

There is a special subdirectory of your home directory called _Desktop_. This directory contains all of the files and folders that are visible on your Mac desktop.

We could say `<span class="pln">$ ls</span> <span class="typ">Desktop</span>` to see all directories located in the `<span class="typ">Desktop</span>` directory, like this:

    epicodus-5:~ Guest$ ls Desktop
    my-coding-project        coding-practice

Here, we can see that our `<span class="typ">Desktop</span>` directory contains two other directories: A folder called `<span class="kwd">my</span><span class="pun">-</span><span class="pln">coding</span><span class="pun">-</span><span class="pln">project</span>` and a folder called `<span class="pln">coding</span><span class="pun">-</span><span class="pln">practice</span>`. (Note that depending on the directories located in _your _`<span class="typ">Desktop</span>` the example response seen above will differ. Again, this is totally normal.)

Or we could run the command `<span class="pln">$ ls</span> <span class="typ">Documents</span>` to see all directories in the `<span class="typ">Documents</span>` directory, like this:

    epicodus-5:~ Guest$ ls Documents
    cover-letters        

Here, we can see this computer has a `<span class="pln">cover</span><span class="pun">-</span><span class="pln">letters</span>` directory in its `<span class="typ">Documents</span>` directory. (Again, the response will differ based on the files and folders present in your specific computer.)

You can also use this command in conjunction with any directory in your current location. That is, you can run `<span class="pln">$ ls</span>` to see all directories in your current location. Then, you can see into any of the directories displayed by running `<span class="pln">$ ls directory</span><span class="pun">-</span><span class="pln">name</span>`. `<span class="pln">directory</span><span class="pun">-</span><span class="pln">name</span>` should be replaced with the name of the folder you'd like to look inside.

## Navigation

So far we've learned how to see what directories are in our current location. And, how to see what directories are inside _those_ directories. But what if we want to see the directories in an entirely different area of our computer? How would we do that?

Thankfully, similar to the way we can navigate around different files and folders in Mac's _Finder_, or Windows' _Explorer_, we can also navigate around our various files and folders directly through the command line. In this section, we will learn commands to navigate through our computer in the Terminal.

### Moving Between Directories with `<span class="pln">$ cd</span>`

`<span class="pln">$ cd</span>` stands for _change directory_. As the name implies, this command allows us to navigate to a different directory. Unlike the commands we've learned so far, this command _requires_ another word or symbol to be included with it. This additional word or symbol tells the terminal _which_ directory we should navigate into.

Let's look at several ways to execute the `<span class="pln">$ cd</span>` command:

### `<span class="pln">$ cd directory</span><span class="pun">-</span><span class="pln">name</span>`

We can include the name of a directory we'd like to navigate to after the `<span class="pln">cd</span>` command. Notice they are separated by a space. For instance, we can run the `<span class="pln">$ ls</span>` command to list all the directories in our area:

    epicodus-5:~ Guest$ ls
    Documents       Library         Pictures
    Applications        Downloads       Movies
    Desktop             Music           Public          

Then, we can navigate into any of these directories by using the `<span class="pln">$ cd</span>` command, along with their name:

    epicodus-5:~ Guest$ cd Documents        

After we run the `<span class="pln">$ cd</span>` command, no text is printed to the screen. This is normal. However, notice that the prompt preceding the command line has changed. It now contains the name of the directory we're currently located in:

    epicodus-5: Documents Guest$ 

Here, the `<span class="pun">~</span>` that was previously displayed has been replaced by the word `<span class="typ">Documents</span>`, because we're currently in the `<span class="typ">Documents</span>` directory. (`<span class="pun">~</span>` means "home directory").

Now that we've navigated elsewhere we can also run the `<span class="pln">$ pwd</span>` command to see our new location:

    epicodus-5:~ Documents Guest$  pwd
    /Users/Guest/Documents

We can include different information after the `<span class="pln">$ cd</span>` command to navigate to different areas. Here are a few examples:

### `<span class="pln">$ cd</span> <span class="pun">..</span>`

Including two dots, like this `<span class="pun">..</span>`, navigates to the directory one level above the current directory. That is, the directory that houses the directory we're currently located in.

If we are in the `<span class="typ">Documents</span>` directory, as we saw in the example above, we could run `<span class="pln">$ pwd</span>` to see our current location:

    epicodus-5:Documents Guest$ pwd
    /Users/Guest/Documents

Then, we could run the command `<span class="pln">$ cd</span> <span class="pun">..</span>` to move up one level. If we ran `<span class="pln">$ pwd</span>` again, we could see that our current location has changed:

    epicodus-5:Documents Guest$ cd ..
    epicodus-5:~ Guest$ pwd
    /Users/Guest

Instead of being located in `<span class="typ">Users</span><span class="pun">/</span><span class="typ">Guest</span><span class="pun">/</span><span class="typ">Documents</span>`, we're now located one level 'up' in the `<span class="typ">Users</span><span class="pun">/</span><span class="typ">Guest</span>` directory.

### `<span class="pln">$ cd</span> <span class="pun">~</span>`

Also, no matter _where_ we are located, we can always return to the home directory (`<span class="str">/Users/</span><span class="typ">Guest</span>` on Epicodus computers) using the `<span class="pln">$ cd</span> <span class="pun">~</span>` command.

For instance, let's say we navigate back to the `<span class="typ">Desktop</span>` directory with the `<span class="pln">cd</span>` command, like this:

    epicodus-5:~ Guest$ cd Desktop      

Then, once in `<span class="typ">Desktop</span>`, we run `<span class="pln">$ ls</span>` to list all directories in that location, like this:

    Epicodus-5:Desktop Guest$ ls
    my-coding-project        coding-practice

We can see there's a directory called `<span class="pln">coding</span><span class="pun">-</span><span class="pln">practice</span>` here. We want to navigate into that. We run the `<span class="pln">$ cd</span>` command again:

    Epicodus-5:Desktop Guest$ cd coding-practice

Now, we're several directories deep. That is, we've navigated through multiple directories to get to our current location. We can return directly back to the home directory by running `<span class="pln">$ cd</span> <span class="pun">~</span>` like this:

    Epicodus-5:coding-practice Guest$ cd ~
    Epicodus-5: ~ Guest$

After running this command, we can see the prompt changed once again. Additionally, if we run `<span class="pln">$ pwd</span>`, we can see our location has changed. We're back in the home directory:

    epicodus-5:~ Guest$ pwd
    /Users/Guest

Isn't this pretty cool? We can travel around our computer using only the command line!

## Creating Files and Folders

In addition to navigating around our directories, we can also create files and folders through the command line! You'll use these commands often to create files and folders to hold your code here at Epicodus.

### Making New Directories with `<span class="pln">$ mkdir</span>`

The `<span class="pln">$ mkdir</span>` command stands for _make directory_. We can use the combination of commands discussed above to navigate to the location we'd like to create a new folder. Then, we can create a new directory by saying `<span class="pln">$ mkdir name</span><span class="pun">-</span><span class="pln">of</span><span class="pun">-</span><span class="pln">directory</span>`. (Replacing `<span class="pln">name</span><span class="pun">-</span><span class="pln">of</span><span class="pun">-</span><span class="pln">directory</span>` with the name you'd like to assign to _your_ specific directory).

For instance, we could navigate to our `<span class="typ">Desktop</span>` directory:

    epicodus-5:~ Guest$ cd Desktop
    epicodus-5:Desktop Guest$ 

And make a new folder on our `<span class="typ">Desktop</span>` called `<span class="pln">intro</span><span class="pun">-</span><span class="pln">to</span><span class="pun">-</span><span class="pln">programming</span>`:

    epicodus-5:Desktop Guest$ mkdir intro-to-programming
    epicodus-5:Desktop Guest$ 

Then, if we run `<span class="pln">$ ls</span>` to list all directories in our current location, we can see the directory we've just created:

    epicodus-5:Desktop staff$ ls
    intro-to-programming         my-coding-project        coding-practice

When we work at Epicodus, we'll want each new project we create to reside in its own dedicated folder. Therefore, we'll use the `<span class="pln">$ mkdir</span>` command to make new directories every time we create a new project.

### Creating New Files with `<span class="pln">$ touch</span> <span class="kwd">new</span><span class="pun">-</span><span class="pln">file</span><span class="pun">-</span><span class="pln">name</span>`

The `<span class="pln">$ touch</span>` command is very similar to `<span class="pln">$ mkdir</span>`, but instead of creating a new _directory_, this command creates a new _file_. For example, we could navigate into the new `<span class="pln">intro</span><span class="pun">-</span><span class="pln">to</span><span class="pun">-</span><span class="pln">programming</span>` directory we just created with the `<span class="pln">$ cd</span>` command:

    epicodus-5:Desktop Guest$ cd intro-to-programming
    epicodus-5:intro-to-programming Guest$ 

Then, we can create a new file called _my-first-project.html_ inside of this directory using `<span class="pln">$ touch</span>`, like this:

    epicodus-5:intro-to-programming Guest$ touch my-first-project.html

Then, we can run `<span class="pln">$ ls</span>` to see that our new file has been created:

    epicodus-5:intro-to-programming Guest$ ls
    my-first-project.html

## Moving Files

In addition to creating directories and files directly through the command line, we can also move them!

### Moving and Renaming Files with `<span class="pln">$ mv file</span><span class="pun">-</span><span class="pln">location</span> <span class="kwd">new</span><span class="pun">-</span><span class="pln">file</span><span class="pun">-</span><span class="pln">location</span>`

The `<span class="pln">$ mv</span>` command stands for _move_. It can both move _and_ rename files. For instance, we can see which files are in our current location with `<span class="pln">$ ls</span>`, like this:

    epicodus-5:intro-to-programming Guest$ ls
    my-first-project.html

As we can see, this directory contains a file called `<span class="kwd">my</span><span class="pun">-</span><span class="pln">first</span><span class="pun">-</span><span class="pln">project</span><span class="pun">.</span><span class="pln">html</span>`. If we wanted to rename this file, we could do this:

    epicodus-5:intro-to-programming Guest$ mv my-first-project.html my-first-webpage.html

As you can see, the `<span class="pln">$ mv</span>` command requires two pieces of information: First, the name of the file we'd like to rename or move. Secondly, the _new_ name or location we'd like to provide the file. So, in the example above, we are renaming a file called `<span class="kwd">my</span><span class="pun">-</span><span class="pln">first</span><span class="pun">-</span><span class="pln">project</span><span class="pun">.</span><span class="pln">html</span>` to `<span class="kwd">my</span><span class="pun">-</span><span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span><span class="pun">.</span><span class="pln">html</span>`.

We can confirm the file has been successfully renamed by using `<span class="pln">$ ls</span>` to list all files in the current location:

    epicodus-5:intro-to-programming Guest$ ls
    my-first-webpage.html

However, let's assume that the `<span class="pln">intro</span><span class="pun">-</span><span class="pln">to</span><span class="pun">-</span><span class="pln">programming</span>` directory will contain all the projects we create for our Intro to Programming course. As you'll learn in class, each project should reside in its _own_ directory. But `<span class="kwd">my</span><span class="pun">-</span><span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span><span class="pun">.</span><span class="pln">html</span>` is sitting directly in the `<span class="pln">intro</span><span class="pun">-</span><span class="pln">to</span><span class="pun">-</span><span class="pln">programming</span>` folder.

As we know, we can create a new directory in the current location with the `<span class="pln">$ mkdir</span>` command, like this:

    epicodus-5:intro-to-programming Guest$ mkdir first-webpage

We can run `<span class="pln">$ ls</span>` to see that the new directory has been added:

    epicodus-5:intro-to-programming Guest$ ls
    first-webpage        my-first-webpage.html

We can see that `<span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span>` is a directory, and `<span class="kwd">my</span><span class="pun">-</span><span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span><span class="pun">.</span><span class="pln">html</span>` is a file, because `<span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span>` does not have a file extension, and `<span class="kwd">my</span><span class="pun">-</span><span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span><span class="pun">.</span><span class="pln">html</span>` does. The `<span class="pun">.</span><span class="pln">html</span>` is a file extension.

Then, we can actually move `<span class="kwd">my</span><span class="pun">-</span><span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span><span class="pun">.</span><span class="pln">html</span>` into the new `<span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span>` directory like this:

    epicodus-5:intro-to-programming Guest$ mv my-first-webpage.html first-webpage/my-first-webpage.html

Here, we use the `<span class="pln">$ mv</span>` command. We provide the name of the file we'd like to move, `<span class="kwd">my</span><span class="pun">-</span><span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span><span class="pun">.</span><span class="pln">html</span>` in our case. Then, separated by a space, we provide the _new_ name and location of the file: `<span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span><span class="pun">/</span><span class="kwd">my</span><span class="pun">-</span><span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span><span class="pun">.</span><span class="pln">html</span>`. By renaming the file from `<span class="kwd">my</span><span class="pun">-</span><span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span><span class="pun">.</span><span class="pln">html</span>` to `<span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span><span class="pun">/</span><span class="kwd">my</span><span class="pun">-</span><span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span><span class="pun">.</span><span class="pln">html</span>`, we are actually _moving_ it into the `<span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span>` directory.

If we run `<span class="pln">$ ls</span>` again, we can see that `<span class="kwd">my</span><span class="pun">-</span><span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span><span class="pun">.</span><span class="pln">html</span>` is no longer listed:

    epicodus-5:intro-to-programming Guest$ ls
    first-webpage        

But, if we navigate into the `<span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span>` directory like this:

    epicodus-5:intro-to-programming Guest$ cd first-webpage

We can run `<span class="pln">$ ls</span>` again to list all content of this directory:

    epicodus-5:first-webpage Guest$ ls
    my-first-webpage.html

And see that the `<span class="kwd">my</span><span class="pun">-</span><span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span><span class="pun">.</span><span class="pln">html</span>` file is now located here. We've successfully moved the file into another directory using the `<span class="pln">$ mv</span>` command.

## Moving and Deleting Content

We also have the option to delete files entirely through the command line.

### Removing Files with `<span class="pln">$ rm file</span><span class="pun">-</span><span class="pln">name</span>`

The `<span class="pln">$ rm</span>` command stands for _remove_ and it allows us to delete a specified file entirely.

For instance, we could use `<span class="pln">$ ls</span>` again, to see all content in our current directory:

    epicodus-5:first-webpage Guest$ ls
    my-first-webpage.html

Then, if we wanted to delete our `<span class="kwd">my</span><span class="pun">-</span><span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span><span class="pun">.</span><span class="pln">html</span>` file, we could do so like this:

    epicodus-5:first-webpage Guest$ rm my-first-webpage.html

Here, we use the `<span class="pln">$ rm</span>` command, and include the name of the file we'd like to delete. If we run `<span class="pln">$ ls</span>` again, we can see it returns nothing. That is because this directory no longer contains _any_ files. We've deleted the only file it had:

    epicodus-5:first-webpage Guest$ ls

### Deleting Directories with `<span class="pln">$ rm</span> <span class="pun">-</span><span class="pln">r directory</span><span class="pun">-</span><span class="pln">name</span>`

We can also use the `<span class="pln">$ rm</span>` command to delete entire directories. Now that our `<span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span>` directory is empty, let's delete it.

Firstly, note that you cannot be located _within_ a directory you are attempting to delete. Therefore, we'll navigate out of our `<span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span>` directory using the `<span class="pln">$ cd</span>` command, like this:

    epicodus-5:first-webpage Guest$ cd ..

If we run `<span class="pln">$ pwd</span>` we can see we're now located back in the `<span class="pln">intro</span><span class="pun">-</span><span class="pln">to</span><span class="pun">-</span><span class="pln">programming</span>` directory that the `<span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span>` directory is located in:

    epicodus-5:intro-to-programming Guest$ pwd
    /Users/Guest/Desktop/intro-to-programming

Now, we can delete the `<span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span>` directory like this:

    epicodus-5:intro-to-programming Guest$ rm -r first-webpage

Notice that to delete an entire directory, we must include `<span class="pun">-</span><span class="pln">r</span>` after the `<span class="pln">rm</span>`. This allows us to delete an entire directory, instead of just a file. We can run `<span class="pln">$ ls</span>` again to view the current contents of the directory, and see that `<span class="pln">first</span><span class="pun">-</span><span class="pln">webpage</span>` is no longer listed. It's been deleted.

Do note that `<span class="pln">$ rm</span> <span class="pun">-</span><span class="pln">r directory</span><span class="pun">-</span><span class="pln">name</span>` actually deletes the directory _and_ all of the files within it. Be very careful with this command.

Make sure to check out the cheat sheet tab of this lesson for terminology from this lesson and command line reference of most frequently used commands!