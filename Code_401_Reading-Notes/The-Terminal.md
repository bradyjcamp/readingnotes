# Linux

## The Command Line

- [A command line is a text based interface to the system.](https://ryanstutorials.net/linuxtutorial/commandline.php)
- When looking at the command line, the order of what you see is the **prompt**, the **command** entered, then after that you see the **arguements** entered. There may also be whats called an **option** before the arguement and starts with a "-" most of the time.
- What follows after the command is run is the results or output.
- You can also use the up or down arrows to autofill your previous commands.

## Basic Navigation

- `ls` is an easy way to peek into the current directory you are on to see what files are inside. This will not enter or open any files but will list what is inside it.
- You can follow `ls` up with the file or directory name and search inside specified folders.
- Paths
  - Paths are hierarchical and start at the **root**. It is started with **/**
  - The two types are Absolute and Relative
    - Absolute paths specify the location comparing to the root directory and begin with a **/**
    - Relative paths specify where we are at currently in the system and **will not** begin with a **/**
  - The tilde(~) is a shortcut and equals what your home directory is.

## More About Files

- I learned that linux is an extensionless system and that the .txt or .png or whatever it may be are not needed and will through an error if you try.

## Manual Pages

- This is a list that explains every command possible on your system.
- I did not know that this was available. All you have to is put `man <command to look up>` in your command line.
- Even more helpful you can do a keyword search using the command `man -k <search term>`.

## File Manipulation

- Here are some common commands for files
  - `mkdir`
    - makes a directory
  - `rmdir`
    - removes a directory
  - `touch <filename>`
    - creates a file
  - `cp`
    - copies a file
  - `mv`
    - moves a file
    - can also be used to rename
  - `rm`
    - remove files and non empty directories
