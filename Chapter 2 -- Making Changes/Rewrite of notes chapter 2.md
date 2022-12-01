## Last time (2.1)
Last set of commands from chapter 1 were for looking around not making changes to anything
![[Rewriting of notes chapter 1#Listing Files ls 1 6-1 8]]

![[Rewriting of notes chapter 1#Changing directories cd 1 5]]

![[Rewriting of notes chapter 1#Displaying the contents of a file 1 13]]

![[Rewriting of notes chapter 1#Displaying a long file 1 14]]

## Editing files (2.2)
You need to be able to create and edit files the normal things is vim for a text editor
![[Pasted image 20220712181814.png]]

## Why vim? (2.3)
Vim is a harder text editor to learn but is really powerful.

Vim pros:
1. Widely available
2. Very powerful editor with minute levels of control
3. Highly customizable

## Two modes (2.4)
Vim has two primary modes

Normal mode: Give commands, move around, copy paste, search, save quit, etc.
Insert mode: You type text into the document directly

How to change between modes:
 1. From normal mode press i to get to insert mode
 2. From insert mode press escape to get back to normal mode


## Vim normal mode: Essentials (2.5)
Things you can do in normal mode:

1. Arrow keys       move around
2. i    insert before the current character
3. dd    cut the current line
4. yy    copy the current line
5. p     paste
6. u     undo
7. Ctrl-R    redo
8. nG     go to line n
9. :w save('write') -- Press enter to finish the command
10. :q    quit -- Press enter to finish the command

## Vim normal mode: A little more (2.6)
More things you can do in normal mode:

1. h,j,k,l    move around
2. x    cut the current character
3. I    insert at the start of the current line
4. A    insert at the end of the line
5. G    go to the end of the file
6. :wq    save and quit -- Press enter to finish the command
7. :q!    quit without saving -- Press enter to finish the command


## Going deeper (2.7)
Vim cheat sheet:
![[Pasted image 20220712184526.png]]

Quick learning with a game: 
![[Pasted image 20220712184551.png]]

##  Some shell keys (2.8)
Moving on from vim, to the shell

A few keys are extremely helpful:
- Left and right arrow to edit the current command
- Up and down arro to go back to previous commands
- tab for autocomplete
- Ctrl-c to kill a command

## Sending command output to a file (2.9)
We can redirect output from a command into a file instead of out terminal windo using > and >> 
![[Pasted image 20220712212140.png]]

Example: >
![[Pasted image 20220712212216.png]]

Example: >>
![[Pasted image 20220712212241.png]]

## Why redirection is cool (2.10)

Gives a change to redirect the output of any file for example running a hello world program will output hello world to the output file so perfect for outputting to reports.
![[Pasted image 20220712212636.png]]

## Showing output (2.11)
Echo - print things on standard output
(you know this command like the back of your hand)

Example use:
![[Pasted image 20220712213117.png]]


## Creating directories
Directories are used to keep files organized
![[Pasted image 20220712213322.png]]

![[Chapter 2 commands#mkdir]]


## Copying files (2.13-2.14)

We can make a copy of files with the cp command

![[Chapter 2 commands#cp]]

Note: The last argument to cp is the destination; everything before that is a list of what to copy

## Moving and renaming (2.15)
mv: used to move and/or rename things
![[Pasted image 20220712214608.png]]
![[Chapter 2 commands#mv]]

## Deleting files (2.16-2.18)
**BE CAREFUL THERE IS NO UNDO, TRASH CAN, AND NO RECYCLING BIN**
RM: deletes and 'removes' files
![[Chapter 2 commands#rm]]


![[Chapter 2 commands#rmdir]]



