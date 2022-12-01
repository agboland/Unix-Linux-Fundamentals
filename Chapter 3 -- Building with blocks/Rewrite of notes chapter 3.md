# Building with Blocks

###  Last time (3.1)

Last time was about creating and changing files and directories
![[Chapter 2 commands]]


### Input and Output (3.2)
Each time we run a program that program has two data streams

1. Input comes from standard input
2. Output goes to standard ouput

![[Pasted image 20220713214011.png]]


### You already know this (3.3)
The programs that I already code with have a way to read from the standard input:
		System.in, cin, read, sys.stdin...

and standard output:
		System.out, cout, print, sys.stdout...


### Typical behavior (3.4)

Usually: 

- Standard input is connected to the keyboard since that is one of the main ways the interactions come when working with linux
- Standard output goes to the terminal window

![[Pasted image 20220713214414.png]]




### Example: A calculator program (3.5)
There is a built in calculator program in linux and it is bc and it reads the arithmetic input and outputs it to the standard output.
![[Pasted image 20220713215314.png]]

![[Chapter 3 commands#bc]]

### Review: Output redirection (3.6)
The standard outut can go to a file instead of a terminal by using > & >> 

![[Pasted image 20220713215740.png]]

Diagram: of path followed
![[Pasted image 20220713215759.png]]

### Input redirection (3.7)

You can pull the standard input from a file using <

![[Pasted image 20220713220253.png]]

Diagram of path followed
![[Pasted image 20220713220348.png]]

**Programs tend to read from standard input until they reach end of file (EOF) and to generate this on youw own press Ctrl-d**


### Examples with bc (3.8)
Input and output redirection things

Diagram of path for output redirection:
![[Pasted image 20220713222024.png]]

diagram of path for input redirection:
![[Pasted image 20220713222049.png]]

Diagram of path for both:
![[Pasted image 20220713222119.png]]

Code examples for all of these:
![[Chapter 3 commands#bc continued]]
Uh oh something broke bc wrong:
![[Pasted image 20220713222152.png]]

See next section for explanation -->

### Standard Error (3.9)
There is a standard input and a standard output so there has to be a standard error!!!!

Programs you use have examples of this:
		System.err, cerr, print(file=sys.stderr,),...

Path thing:
![[Pasted image 20220713224302.png]]

**Important:** Standard error shows error messages even when not looking at the standard output

### Error redirection (3.10)
Errors can be redirected like everything else! 
It is done by using 2> & 2>>

![[Pasted image 20220713224601.png]]

path thingy again:
![[Pasted image 20220713224625.png]]






### Example: Catching compile errors (3.11)
A bad C++ program throws a lot of errors! Here is a mild? example:
![[Pasted image 20220713225109.png]]

But instead of it being that mess above (which looks like my normal code btw) send it to a file for you to look at the errors closer and neater!
![[Pasted image 20220713225446.png]]


### Multiple commands (3.12)
If we want the output of one program to be the input of another program we can do this thing but it uses a lot of steps:
![[Pasted image 20220713225656.png]]

Pros: 
- Good for pea brain
Cons:
- Three steps so has 3 chances to mess up
- The program runs each step one at a time so slow
- Has to keep track of temp file

### Pipes (3.13)
A pipe runs two or more commands connect the standard output of each command to the standard input of the next so works like previous way of doing things.
![[Chapter 3 commands#Pipe]]

Pros:
- One compact line
- Faster: Can start processing its input while the other is producing more output
- No temp files data flow from one to another directly
Cons: 
- not good for pea brain

You can also do MORE THAN TWO COMMANDS!!

### Filters (3.14-3.17)
A program that is designed to be used in pipelines is called a filter. There are lots of them some are below

![[Chapter 3 commands#Pipe Filters]]