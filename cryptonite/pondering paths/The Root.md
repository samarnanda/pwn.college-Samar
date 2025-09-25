# The Root
This challenge asks you to invoke the "pwn" program by providing its absolute path on the command line and obtain the flag.
# My Solve
**Flag**-pwn.college{g7A-ZinbI0reCFyz0QM2epda7qf.QX4cTO0wyN5EzNzEzW}

The "/" is used to invoke the file system. To invoke the "pwn" program, we type "/pwn" into the command line and obtain the flag.
>hacker@paths~the-root:~$ /pwn
>BOOM!!!
>Here is your flag:
>pwn.college{g7A-ZinbI0reCFyz0QM2epda7qf.QX4cTO0wyN5EzNzEzW}

# What I learned
I learned that the file system starts at "/" and under that, there is a whole mess of diffrent directories such as configuration files, program files etc.
We can invoke a program by providing its path on the command line. In "/pwn" we have provided the exact path starting from "/".
This type of path which starts at the root directory is called the "absolute path".

# References
None.
