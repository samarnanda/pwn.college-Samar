# Multi-word variables
This challenge asks us to set a variable with a value, but the value has a space character. Once we are successful we get the flag.
# My solve
**Flag**-pwn.college{YaWHit8Ypjgx0Jvr3eyyx0kIIaD.QXwYTN0wyN5EzNzEzW}

>hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"

>You've set the PWN variable properly! As promised, here is the flag:

>pwn.college{YaWHit8Ypjgx0Jvr3eyyx0kIIaD.QXwYTN0wyN5EzNzEzW}

# What I learned
When the shell sees a space, it ends the variable assignment and interprets the next word as a command. So, we quote the value of the variable inside " ".

# Reference
None.
