# Reading Files
This challenge asks us to read a program into an environment variable using "read" to obtain the flag.
# My solve
**Flag**-pwn.college{E80e2Te95t-2vkG-ucUcYhmE8WH.QXwIDO0wyN5EzNzEzW}

>hacker@variables~reading-files:~$ read PWN < /challenge/read_me

>You've set the PWN variable properly! As promised, here is the flag:

>pwn.college{E80e2Te95t-2vkG-ucUcYhmE8WH.QXwIDO0wyN5EzNzEzW}

# What I learned
We can redirect the file into the standard input of read, so when **read** reads into the variable, it reads from the file.
# Reference
None.
