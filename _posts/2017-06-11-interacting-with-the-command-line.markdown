---
layout: post
title: "Interacting With the Command Line"
tags: 
date: 2017-06-11T00:54:24-05:00
---
In the last lesson we learned about the terminal and its command line; including how to access and install it, and the notation commands are commonly conveyed in. Now, let's learn the specific commands we can execute to interact with our computer directly through the command line.

In this lesson we'll explore the most common commands executed through the command line. You'll use many of these _daily_ during the program.

## Basics

To enter a command we simply click within the terminal window and begin typing. Text will be inserted where our cursor is located, directly after the prompt. Then, after typing a command we can press enter to run it.

Let's look at some of these commands now.

### Retrieving Current Location with `$ pwd`

The `$ pwd` command prints your current location to the screen. `pwd` stands for _print working directory_.

Remember, similar to the Mac _Finder_ or Windows _Explore_ program, the command line allows us to look around our computer. We can navigate through folders and directories and see what's inside. The only difference is that _Finder_ and _Explore_ have graphical user interfaces, and the terminal does not.

So, by entering `pwd` into the command line and pressing enter, we can get our current location. It returns a file **path**, like this:

    techmill-5:~ Guest$ pwd
    /Users/Guest

In the example above we typed `pwd` right after our command prompt. The terminal responded by printing out our current location for us. As you can see, we're located in the `Users` directory, in a folder called `Guest`.

When you open the Terminal application on a Mac, you will begin in your home directory. For example, if your username is Jesse, your home directory is _/Users/Jesse_. You can verify this by typing `pwd` at the command prompt and pressing Enter.

If you're navigating through files and folders in the command line and are unsure of your current location, you can always run the `$ pwd` command. It's like a _"You are here"_. Give this command a shot now.

### Listing All Content with `$ ls`

The `$ ls` command stands for _list_. Executing this command prompts the terminal to list out the directories (directories is just a technical term for folders) and files in our current location. Running this command looks something like this:

    techmill-5:~ Guest$ ls
    Documents       Library         Pictures
    Applications        Downloads       Movies
    Desktop             Music           Public          

We can also list out the directories _inside_ of one of these directories by including its name after the `$ ls` command. The command and specific directory name should be separated by a space.

There is a special subdirectory of your home directory called _Desktop_. This directory contains all of the files and folders that are visible on your Mac desktop.

We could say `$ ls Desktop` to see all directories located in the `Desktop` directory, like this:

    techmill-5:~ Guest$ ls Desktop
    my-coding-project        coding-practice

Here, we can see that our `Desktop` directory contains two other directories: A folder called `my-coding-project` and a folder called `coding-practice`. (Note that depending on the directories located in _your _`Desktop` the example response seen above will differ. Again, this is totally normal.)

Or we could run the command `$ ls Documents` to see all directories in the `Documents` directory, like this:

    techmill-5:~ Guest$ ls Documents
    cover-letters        

Here, we can see this computer has a `cover-letters` directory in its `Documents` directory. (Again, the response will differ based on the files and folders present in your specific computer.)

You can also use this command in conjunction with any directory in your current location. That is, you can run `$ ls` to see all directories in your current location. Then, you can see into any of the directories displayed by running `$ ls directory-name`. `directory-name` should be replaced with the name of the folder you'd like to look inside.

## Navigation

So far we've learned how to see what directories are in our current location. And, how to see what directories are inside _those_ directories. But what if we want to see the directories in an entirely different area of our computer? How would we do that?

Thankfully, similar to the way we can navigate around different files and folders in Mac's _Finder_, or Windows' _Explorer_, we can also navigate around our various files and folders directly through the command line. In this section, we will learn commands to navigate through our computer in the Terminal.

### Moving Between Directories with `$ cd`

`$ cd` stands for _change directory_. As the name implies, this command allows us to navigate to a different directory. Unlike the commands we've learned so far, this command _requires_ another word or symbol to be included with it. This additional word or symbol tells the terminal _which_ directory we should navigate into.

Let's look at several ways to execute the `$ cd` command:

### `$ cd directory-name`

We can include the name of a directory we'd like to navigate to after the `cd` command. Notice they are separated by a space. For instance, we can run the `$ ls` command to list all the directories in our area:

    techmill-5:~ Guest$ ls
    Documents       Library         Pictures
    Applications        Downloads       Movies
    Desktop             Music           Public          

Then, we can navigate into any of these directories by using the `$ cd` command, along with their name:

    techmill-5:~ Guest$ cd Documents        

After we run the `$ cd` command, no text is printed to the screen. This is normal. However, notice that the prompt preceding the command line has changed. It now contains the name of the directory we're currently located in:

    techmill-5: Documents Guest$ 

Here, the `~` that was previously displayed has been replaced by the word `Documents`, because we're currently in the `Documents` directory. (`~` means "home directory").

Now that we've navigated elsewhere we can also run the `$ pwd` command to see our new location:

    techmill-5:~ Documents Guest$  pwd
    /Users/Guest/Documents

We can include different information after the `$ cd` command to navigate to different areas. Here are a few examples:

### `$ cd ..`

Including two dots, like this `..`, navigates to the directory one level above the current directory. That is, the directory that houses the directory we're currently located in.

If we are in the `Documents` directory, as we saw in the example above, we could run `$ pwd` to see our current location:

    techmill-5:Documents Guest$ pwd
    /Users/Guest/Documents

Then, we could run the command `$ cd ..` to move up one level. If we ran `$ pwd` again, we could see that our current location has changed:

    techmill-5:Documents Guest$ cd ..
    techmill-5:~ Guest$ pwd
    /Users/Guest

Instead of being located in `Users/Guest/Documents`, we're now located one level 'up' in the `Users/Guest` directory.

### `$ cd ~`

Also, no matter _where_ we are located, we can always return to the home directory (`/Users/Guest` on Epicodus computers) using the `$ cd ~` command.

For instance, let's say we navigate back to the `Desktop` directory with the `cd` command, like this:

    techmill-5:~ Guest$ cd Desktop      

Then, once in `Desktop`, we run `$ ls` to list all directories in that location, like this:

    techmill-5:Desktop Guest$ ls
    my-coding-project        coding-practice

We can see there's a directory called `coding-practice` here. We want to navigate into that. We run the `$ cd` command again:

    techmill-5:Desktop Guest$ cd coding-practice

Now, we're several directories deep. That is, we've navigated through multiple directories to get to our current location. We can return directly back to the home directory by running `$ cd ~` like this:

    techmill-5:coding-practice Guest$ cd ~
    techmill-5: ~ Guest$

After running this command, we can see the prompt changed once again. Additionally, if we run `$ pwd`, we can see our location has changed. We're back in the home directory:

    techmill-5:~ Guest$ pwd
    /Users/Guest

Isn't this pretty cool? We can travel around our computer using only the command line!

## Creating Files and Folders

In addition to navigating around our directories, we can also create files and folders through the command line! You'll use these commands often to create files and folders to hold your code here at Epicodus.

### Making New Directories with `$ mkdir`

The `$ mkdir` command stands for _make directory_. We can use the combination of commands discussed above to navigate to the location we'd like to create a new folder. Then, we can create a new directory by saying `$ mkdir name-of-directory`. (Replacing `name-of-directory` with the name you'd like to assign to _your_ specific directory).

For instance, we could navigate to our `Desktop` directory:

    techmill-5:~ Guest$ cd Desktop
    techmill-5:Desktop Guest$ 

And make a new folder on our `Desktop` called `intro-to-programming`:

    techmill-5:Desktop Guest$ mkdir intro-to-programming
    techmill-5:Desktop Guest$ 

Then, if we run `$ ls` to list all directories in our current location, we can see the directory we've just created:

    techmill-5:Desktop staff$ ls
    intro-to-programming         my-coding-project        coding-practice

When we work at Epicodus, we'll want each new project we create to reside in its own dedicated folder. Therefore, we'll use the `$ mkdir` command to make new directories every time we create a new project.

### Creating New Files with `$ touch new-file-name`

The `$ touch` command is very similar to `$ mkdir`, but instead of creating a new _directory_, this command creates a new _file_. For example, we could navigate into the new `intro-to-programming` directory we just created with the `$ cd` command:

    techmill-5:Desktop Guest$ cd intro-to-programming
    techmill-5:intro-to-programming Guest$ 

Then, we can create a new file called _my-first-project.html_ inside of this directory using `$ touch`, like this:

    techmill-5:intro-to-programming Guest$ touch my-first-project.html

Then, we can run `$ ls` to see that our new file has been created:

    techmill-5:intro-to-programming Guest$ ls
    my-first-project.html

## Moving Files

In addition to creating directories and files directly through the command line, we can also move them!

### Moving and Renaming Files with `$ mv file-location new-file-location`

The `$ mv` command stands for _move_. It can both move _and_ rename files. For instance, we can see which files are in our current location with `$ ls`, like this:

    techmill-5:intro-to-programming Guest$ ls
    my-first-project.html

As we can see, this directory contains a file called `my-first-project.html`. If we wanted to rename this file, we could do this:

    techmill-5:intro-to-programming Guest$ mv my-first-project.html my-first-webpage.html

As you can see, the `$ mv` command requires two pieces of information: First, the name of the file we'd like to rename or move. Secondly, the _new_ name or location we'd like to provide the file. So, in the example above, we are renaming a file called `my-first-project.html` to `my-first-webpage.html`.

We can confirm the file has been successfully renamed by using `$ ls` to list all files in the current location:

    techmill-5:intro-to-programming Guest$ ls
    my-first-webpage.html

However, let's assume that the `intro-to-programming` directory will contain all the projects we create for our Intro to Programming course. As you'll learn in class, each project should reside in its _own_ directory. But `my-first-webpage.html` is sitting directly in the `intro-to-programming` folder.

As we know, we can create a new directory in the current location with the `$ mkdir` command, like this:

    techmill-5:intro-to-programming Guest$ mkdir first-webpage

We can run `$ ls` to see that the new directory has been added:

    techmill-5:intro-to-programming Guest$ ls
    first-webpage        my-first-webpage.html

We can see that `first-webpage` is a directory, and `my-first-webpage.html` is a file, because `first-webpage` does not have a file extension, and `my-first-webpage.html` does. The `.html` is a file extension.

Then, we can actually move `my-first-webpage.html` into the new `first-webpage` directory like this:

    techmill-5:intro-to-programming Guest$ mv my-first-webpage.html first-webpage/my-first-webpage.html

Here, we use the `$ mv` command. We provide the name of the file we'd like to move, `my-first-webpage.html` in our case. Then, separated by a space, we provide the _new_ name and location of the file: `first-webpage/my-first-webpage.html`. By renaming the file from `my-first-webpage.html` to `first-webpage/my-first-webpage.html`, we are actually _moving_ it into the `first-webpage` directory.

If we run `$ ls` again, we can see that `my-first-webpage.html` is no longer listed:

    techmill-5:intro-to-programming Guest$ ls
    first-webpage        

But, if we navigate into the `first-webpage` directory like this:

    techmill-5:intro-to-programming Guest$ cd first-webpage

We can run `$ ls` again to list all content of this directory:

    techmill-5:first-webpage Guest$ ls
    my-first-webpage.html

And see that the `my-first-webpage.html` file is now located here. We've successfully moved the file into another directory using the `$ mv` command.

## Moving and Deleting Content

We also have the option to delete files entirely through the command line.

### Removing Files with `$ rm file-name`

The `$ rm` command stands for _remove_ and it allows us to delete a specified file entirely.

For instance, we could use `$ ls` again, to see all content in our current directory:

    techmill-5:first-webpage Guest$ ls
    my-first-webpage.html

Then, if we wanted to delete our `my-first-webpage.html` file, we could do so like this:

    techmill-5:first-webpage Guest$ rm my-first-webpage.html

Here, we use the `$ rm` command, and include the name of the file we'd like to delete. If we run `$ ls` again, we can see it returns nothing. That is because this directory no longer contains _any_ files. We've deleted the only file it had:

    techmill-5:first-webpage Guest$ ls

### Deleting Directories with `$ rm -r directory-name`

We can also use the `$ rm` command to delete entire directories. Now that our `first-webpage` directory is empty, let's delete it.

Firstly, note that you cannot be located _within_ a directory you are attempting to delete. Therefore, we'll navigate out of our `first-webpage` directory using the `$ cd` command, like this:

    techmill-5:first-webpage Guest$ cd ..

If we run `$ pwd` we can see we're now located back in the `intro-to-programming` directory that the `first-webpage` directory is located in:

    techmill-5:intro-to-programming Guest$ pwd
    /Users/Guest/Desktop/intro-to-programming

Now, we can delete the `first-webpage` directory like this:

    techmill-5:intro-to-programming Guest$ rm -r first-webpage

Notice that to delete an entire directory, we must include `-r` after the `rm`. This allows us to delete an entire directory, instead of just a file. We can run `$ ls` again to view the current contents of the directory, and see that `first-webpage` is no longer listed. It's been deleted.

Do note that `$ rm -r directory-name` actually deletes the directory _and_ all of the files within it. Be very careful with this command.

Make sure to check out the cheat sheet tab of this lesson for terminology from this lesson and command line reference of most frequently used commands!