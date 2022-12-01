# Basics
## The shell (1.1)
When giving commands in the terminal window you are interacting with the shell.
Usually you run other programs.
A few different shells:
- bash
- csh
- fish
- sh
- tcsh
- zsh
- and more ...

## Files and directories (1.2)
Files are in a Hierarchy of directories (folders like you are used to from windows):
![[Pasted image 20220711215345.png]]
Every user has a home directory -- looks the same as a user profile in windows
All named and is case sensitive

## The root directory (1.3)
All files have a starting point of the home directory -- Shows as the same as C: drive on windows
![[Pasted image 20220711215759.png]]

## The current directory (1.4)
Each program has a working directory
Commands all start in the current directory

![[Chapter 1 commands#Print Working Directory]]

**You need to use this  command often to double check what you are doing or editing**

## Changing directories: cd (1.5)
To navigate the current directory use the cd command which stands for change directory.

![[Pasted image 20220711221504.png]]

![[Chapter 1 commands#Change Directory]]

## Listing Files: ls (1.6-1.8)
For you to view the files in the current directory or a specific child directory that you start

![[Pasted image 20220711222437.png]]

![[Chapter 1 commands#ls]]

## Special directory names (1.9)
Several important shortcuts for referring to certain directories
-   .  Current directory
-   .. Parent directory
-   ~ Home directory
-   /  Root directory

## Absolute and relative paths (1.10)
Relative path: Starting from the current directory
![[Pasted image 20220711225853.png]]
![[Pasted image 20220711225918.png]]
Start with / to get an absolute path which starts from the root directory
![[Pasted image 20220711230841.png]]
Use a ~ for the home directory
![[Pasted image 20220711230929.png]]

## Examples with cd (1.11)
![[Pasted image 20220711231016.png]]

## Remember (1.12)
Use ls for what is in the directory 
Use cd to go to a different directory

## Displaying the contents of a file (1.13)
To see what is in a file use the cat command which stands for concatenate
![[Pasted image 20220711232041.png]]

![[Chapter 1 commands#cat]]

## Displaying a long file (1.14)
Sometimes a file is too long for the cat command

The less command comes in handy here for you  to scroll and do other things as shown below once it pulls you into the interactive file
![[Pasted image 20220711233251.png]]

![[Chapter 1 commands#less]]

## Getting more information (1.15)
Linux systems have a manual built in as a command it is for man the commands that are in linux you can use man to get more information on the command. It also opens like a less command essentially so same interactives as above.

![[Pasted image 20220711234446.png]]

![[Chapter 1 commands#man]]