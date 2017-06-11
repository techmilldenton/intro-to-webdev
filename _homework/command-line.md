---
layout: post
title: "Practice: Command Line"
---
## Warm up

* * *

_Ask yourself the following questions before moving on:_

*   What is the difference between a graphical user interface and a command line interface?
*   What makes a home directory a _home_ directory instead of just a directory or subdirectory?
*   Why do we use a text editor instead of a word processing program for writing programs?

## Code

* * *

Now that you have some of the basics of the command line down, let's practice using those new skills to navigate in the terminal.

_Complete the following exercises in your computer's Terminal shell:_

1.  Open a terminal shell. This will be your home directory. You should have a `<span class="pln">$</span>` at the end of the prompt. In our lessons, we will begin the code meant for the command line with a `<span class="pln">$</span>`. You will only type what follows the `<span class="pln">$</span>`, not the `<span class="pln">$</span>` itself. You are now ready to use the command line!

2.  Run the command `<span class="pln">$ pwd</span>`. The computer will print the pathname to the directory that you are currently located in. For example, you might see _/Users/Guest_.

3.  Now let's figure out what directories reside in our home directory by running the command `<span class="pln">$ ls</span>` to list all of the directories and files in the current working directory.

4.  Move into the _Desktop_ directory by running the command `<span class="pln">$ cd</span> <span class="typ">Desktop</span>`. Now run `<span class="pln">$ ls</span>` again to see all of the files and folders located on your computer's desktop.

5.  Now that we have entered a few commands, use the _up_ and _down_ arrow keys to navigate to previous commands you've entered.

6.  Let's make a new folder on the desktop. Run `<span class="pln">$ pwd</span>` to make sure you are in the Desktop directory. If not, navigate to the _Desktop_ directory by running `<span class="pln">$ cd</span> <span class="typ">Desktop</span>`.

7.  Then, run `<span class="pln">$ mkdir test</span>`. This will make a new directory on your desktop called _test_. Take a look and make sure it is there! You can make multiple directories at the same time by putting a _space_ between the directories names. For example, `<span class="pln">$ mkdir test test2</span>`.

8.  Move into the _test_ directory through the command line.

9.  Run `<span class="pln">$ touch file1 file2</span>` to create two new files within the _test_ directory called _file1_ and _file 2_. The `<span class="pln">touch</span>` command creates a new, empty file.

*   If you're using Windows PowerShell, you can use the command `<span class="pun">></span> <span class="pln"></span> <span class="typ">New</span><span class="pun">-</span><span class="typ">Item</span>` or the alias `<span class="pun">></span> <span class="pln">ni</span>` instead of `<span class="pln">$ touch</span>`. (Note that, by default, Windows will only let you create one new file at a time.)

1.  Type `<span class="pln">ls</span>` to make sure that the files are there. Just like making directories, you can make multiple files at the same time.

2.  Run `<span class="pln">$ touch test2</span><span class="pun">/</span><span class="pln">file1 test2</span><span class="pun">/</span><span class="pln">file2</span>` to make files in the _test2_ directory. Oops! That didn't work! Why? Well the terminal can only access the directory above the current working directory and any files/directories in the current working directory. Since _test2_ is a directory in the _Desktop_ directory, we cannot access it from the _test_ directory. In order to do that we need to run the command `<span class="pln">$ touch</span> <span class="pun">../</span><span class="pln">test2</span><span class="pun">/</span><span class="pln">file1</span> <span class="pun">../</span><span class="pln">test2</span><span class="pun">/</span><span class="pln">file2</span>`. This path tells the terminal to go up to the _Desktop_ - using the `<span class="pun">..</span>` command - and then back down to the _test2_ folder. Notice that we just made two files in a directory that we were not currently in! This works because we supplied the directories we wanted those files to be created in.

3.  Let's navigate back to the _Desktop_. _Desktop_ is the parent of our current working directory, so we can use the command `<span class="pln">$ cd</span> <span class="pun">..</span>`. If we wanted to go back to our home directory, we can always use the command `<span class="pln">$ cd</span> <span class="pun">~</span>`.

4.  Let's remove the `<span class="pln">test</span>` directory. Run `<span class="pln">$ rm test</span>`.

5.  You should get the error `<span class="pln">rm</span><span class="pun">:</span> <span class="pln">test</span><span class="pun">:</span> <span class="pln"></span> <span class="kwd">is</span> <span class="pln">a directory</span>`. This means that because there are files in the directory, you can't just delete it without deleting all of the files first. To do that, run the command `<span class="pln">$ rm</span> <span class="pun">-</span><span class="pln">r test</span>`. This will use the **recursive** option to instruct the computer to delete everything in the `<span class="pln">test</span>` folder, including the folder itself.

6.  Now let's exit the terminal by typing `<span class="pln">$</span> <span class="kwd">exit</span>`.

**More command line (terminal) practice on your own:** Make a folder on your desktop that contains 3 subfolders and in each of those subfolders add in 3 individual files. Get comfortable doing this step by step, but then try to do it in as few commands as possible. Then go through and practice deleting files and folders. Make sure you're comfortable navigating around and creating and deleting both files and directories before moving on.