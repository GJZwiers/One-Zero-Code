# Interacting with Terminals

> In this guide you will learn how to use an operating system's terminal to navigate the filesystem and execute commands.

As you might know, the two most used operating systems today are `Windows` and `Linux`. Each of these systems allows programmers to work with the computer through the `command line` or `terminal`.

What are the advantages of using a plain text screen over a Graphical User Interface (GUI)? Firstly, to use computer systems that come without graphical interfaces. This is often the case for servers running a Linux system.  
Secondly, to make use of the many Command Line Interfaces (CLIs) available to developers. Even though some of them have GUIs as well, these do not always offer the full set of features as a CLI for the same tool.  
Thirdly, for operations on large numbers of files. This is in line with the `Don't Repeat Yourself` principle. Need to rename a thousand images? Terminals have commands available for such tasks.

Their most basic forms are `Command Prompt` for Windows and `shell` for Linux, though many users prefer the more fully-featured `PowerShell` and `Bash` terminals.


The terminal allows you to navigate the filesystem and execute commands without needing a graphical interface. Many software tools come with `Command Line Interfaces` (CLIs) to provide developers with a list of commands to do all kinds of programming-related tasks. In addition, terminals come with `scripting languages` that offer ways to automate common tasks: `shell scripts` for Linux and `batch scripts` for Windows.


To enable tab auto-completion type this in a PowerShell window:
```powershell
Set-PSReadlineKeyHandler -Key Tab -Function MenuComplete
```

## Navigating
You can `c`hange `d`irectory with `cd`.

`.` is an alias for the current directory and `..` is an alias for the directory one level up. So if we were in `/users/bigtimeuser/images/` and type `cd ..` we end up in `/users/bigtimeuser/`.

```bash
cd mydirectory

cd .

cd ..
```

## Completing File Names Automatically



## Finding Files and Text
Find a file location with `find`. The following example searches the filesystem for a file named `cat.jpg`, starting in the current directory and its subdirectories.

```bash
find . -name "cat.jpg"
```

## Displaying Text
The `cat` command (`cat`enate) displays the contents of a file to the terminal as one long chain. Useful for showing relatively short files such as configuration files.

To page through a file one screen at a time you can use `more`. Using this command you can view _more_ than when using `cat`, because `cat` will only show the last part a file if it is quite long.

Then there is the `less` command, which has more features than `more`.

In my opinion the naming of these three commands makes very little sense. They break an important programming principle: `say what you mean`. No one can tell intuitively that `less` is a command for printing file contents to the screen. A name like `show` or `print` would be a much more logical name for this command.