# Application Levels

When programmers write code in languages such as Python or Rust, that code is not yet ready to be run by a computer. Strange as it may sound, high-level programming languages are meant for human eyes. To run code it has to be translated to a form that a Central Processing Unit (CPU) and/or Graphical Processing Unit (GPU) can work with. This format is called binary and its smallest unit is a bit which can have a value of 0 or 1. Bits are organised in bytes which consist of 8 bits. Larger collections of bytes are called kilobytes, megabytes, gigabytes and terabytes. 

Two types of programs convert code to binary form: compilers and interpreters. The former converts all the code to binary before running any of it, while the latter converts and runs it one line at a time.


                 superset
                high-level
                 assembly
                  binary
                    CPU      


# An Atomic Model of Programs
There is a saying I have heard many times and that I have found unhelpful: getting to the bottom of it. 
The issue with this statement is that without any definition of the 'bottom', it can take a long while to get there.  
Let me illustrate what I mean. Say we are writing code and someone proclaims the importance of understanding code all the way to the bottom. This means we have to learn high-level code, move down, learn assembly code, move down, learn machine code, move down, learn about hardware, move down, learn about semiconductors, move down, learn about electricity, move down, learn about electrons and sub-atomic particles, move down, and finally, learn about quantum mechanics, the bottom of all things at least as far as understanding goes today.

Some languages sit closer to the core.  
A shell of high-level languages, some of which sit closer, while others sit further away.


outer shell: Frameworks, Libraries, Applications  
out shell: High-level langs, supersets  
mid shell: compilers, runtimes  
