## Last time (4.1)

Learned about standard input, output, and error.
How to redirect them and pipe them.
![[Rewrite of notes chapter 3#Input and Output 3 2]]
![[Rewrite of notes chapter 3#Review Output redirection 3 6]]
![[Rewrite of notes chapter 3#Input redirection 3 7]]


From now on we will learn some ways to use the shell more efficiently ie the **How to be lazy** 
- Command line arguments and special characters that influence them
- Lists that connect multiple commands to be run independently
- Command substitutions that use the output of one command as arguments for another

## Command line arguments (4.2)
When you type commands you are communicating with a special program called a shell, whose job is to read, interpret, and execute the commands you give usually by running other programs.

The shell passes command line arguments to the program it runs.

Example of arguments and their uses / how they work

![[Pasted image 20220715212940.png]]

## Using the arguments (4.3)
The arguments are available to the program being run, in a form that depends on the programming language. 

Example of Java:
![[Pasted image 20220715213102.png]]

Some of the examples below use a similar program, written as a shell script called showargs

## Special characters (4.4)
Usually, the shell gets arguments by splitting the command up at spaces. So looks like this normally:
command argument argument

However most forms of punctuation are treated as special characters that can change this behavior with lets say:
<  > |  ~

There are a few others and they are important but we haven't made our way to them yet but are about to.

## Wildcards! (4.5)

Arguments that contain * or  ? are placed with a list of filenames that match.
- A ? matches any single character.
- A * matches any sequence of characters.

The characters  * and ? are called wildcards.

Examples in a directory filled with C++, header, and object files:

![[Pasted image 20220715213925.png]]

## Wildcard example (4.6)
Say we wanted a list of all files in a directory that start with the letter 'A' and have a cpp extension. The argument for that would look like:

a*.cpp 

Step by step explanation:
![[Pasted image 20220715214127.png]]

Work of it in use:
![[Pasted image 20220715214156.png]]

## Braces (4.7)

Arguments containing curly braces are replaced with a list of each of the thins between braces.

Example of how it works and looks:
![[Pasted image 20220715221449.png]]
![[Pasted image 20220715221516.png]]


## Tilde for home directory (4.8)

The tilde character (~) is replaced with the path to the user's home directory

![[Pasted image 20220715221631.png]]

## Quotation marks (4.9)

Double quotation marks prevent the shell form:
- splitting into separate arguments 
- expanding wildcards

Example:
![[Pasted image 20220715221750.png]]

## Backslash (4.10)

Use a backslash ![[Pasted image 20220715222008.png]] to force the next character to be treated normally. This is called 'escaping' the character

Normal not escaped:
![[Pasted image 20220715221933.png]]

Escaped:
![[Pasted image 20220715222143.png]]

In use with escaping:
![[Pasted image 20220715222218.png]]

In use without escaping:
![[Pasted image 20220715222244.png]]

## Connecting commands (4.11)

Use ; to separate two commands, when each one should be executed

![[Pasted image 20220715222358.png]]

Use && to separate two commands, when the second should be ignored if the first fails.

![[Pasted image 20220715222501.png]]

Use || to separate two commands, when the second should be executed if the first fails. *Use this to set a fail marker in scripting*

![[Pasted image 20220715222647.png]]

1. ; is used for running two commands
2. && is used for running two commands and should be used if ; doesn't work
3. || used to separate two commands and to set for something to run if it fails.

## Compile and run (4.12)

A useful pattern for running programs is:

Compile command && run command

![[Pasted image 20220715223000.png]]

## Command substitution (4.13)

Use $( ) to insert the output of one command into the arguments for another command.

**Nested Commands!!!!**

Example of how to copy a program:
![[Pasted image 20220715223208.png]]

Example of how to look for a file by name:

![[Pasted image 20220715223246.png]]

## Other special characters (4.14)

A few other special characters that bash treats in special way and what they are/do will follow for the ones not explained.

1. Parentheses ()
2. Square brackets []
3.  Comment # 
4. Variable $
5. Run in background &
6. Negation !
7. ...

