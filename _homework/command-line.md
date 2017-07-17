---
layout: post
title: "Command Line"
icon: terminal
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

1.  Open a terminal shell. This will be your home directory. You should have a `$` at the end of the prompt. In our lessons, we will begin the code meant for the command line with a `$`. You will only type what follows the `$`, not the `$` itself. You are now ready to use the command line!

2.  Run the command `$ pwd`. The computer will print the pathname to the directory that you are currently located in. For example, you might see _/Users/Guest_.

3.  Now let's figure out what directories reside in our home directory by running the command `$ ls` to list all of the directories and files in the current working directory.

4.  Move into the _Desktop_ directory by running the command `$ cd Desktop`. Now run `$ ls` again to see all of the files and folders located on your computer's desktop.

5.  Now that we have entered a few commands, use the _up_ and _down_ arrow keys to navigate to previous commands you've entered.

6.  Let's make a new folder on the desktop. Run `$ pwd` to make sure you are in the Desktop directory. If not, navigate to the _Desktop_ directory by running `$ cd Desktop`.

7.  Then, run `$ mkdir test`. This will make a new directory on your desktop called _test_. Take a look and make sure it is there! You can make multiple directories at the same time by putting a _space_ between the directories names. For example, `$ mkdir test test2`.

8.  Move into the _test_ directory through the command line.

9.  Run `$ touch file1 file2` to create two new files within the _test_ directory called _file1_ and _file 2_. The `touch` command creates a new, empty file.

    *   If you're using Windows PowerShell, you can use the command `>  New-Item` or the alias `> ni` instead of `$ touch`. (Note that, by default, Windows will only let you create one new file at a time.)

1.  Type `ls` to make sure that the files are there. Just like making directories, you can make multiple files at the same time.

2.  Run `$ touch test2/file1 test2/file2` to make files in the _test2_ directory. Oops! That didn't work! Why? Well the terminal can only access the directory above the current working directory and any files/directories in the current working directory. Since _test2_ is a directory in the _Desktop_ directory, we cannot access it from the _test_ directory. In order to do that we need to run the command `$ touch ../test2/file1 ../test2/file2`. This path tells the terminal to go up to the _Desktop_ - using the `..` command - and then back down to the _test2_ folder. Notice that we just made two files in a directory that we were not currently in! This works because we supplied the directories we wanted those files to be created in.

3.  Let's navigate back to the _Desktop_. _Desktop_ is the parent of our current working directory, so we can use the command `$ cd ..`. If we wanted to go back to our home directory, we can always use the command `$ cd ~`.

4.  Let's remove the `test` directory. Run `$ rm test`.

5.  You should get the error `rm: test:  is a directory`. This means that because there are files in the directory, you can't just delete it without deleting all of the files first. To do that, run the command `$ rm -r test`. This will use the **recursive** option to instruct the computer to delete everything in the `test` folder, including the folder itself.

6.  Now let's exit the terminal by typing `$ exit`.

**More command line (terminal) practice on your own:** Make a folder on your desktop that contains 3 subfolders and in each of those subfolders add in 3 individual files. Get comfortable doing this step by step, but then try to do it in as few commands as possible. Then go through and practice deleting files and folders. Make sure you're comfortable navigating around and creating and deleting both files and directories before moving on.