# The PATH Variable
This challenge asks us to disrupt the operation of a program. This program deletes the flag using the "rm" command. So we need to make it so that the program cannot find the "rm" command, thus not deleting the flag when run. We use the PATH variable for this.
# My solve
**Flag**-pwn.college{gmt88ooMBHTpVAJBEGBK6YgqS7g.QX2cDM1wyN5EzNzEzW}

>hacker@path~the-path-variable:~$ export PATH=""

>hacker@path~the-path-variable:~$ /challenge/run

>Trying to remove /flag...

>/challenge/run: line 4: rm: No such file or directory

>The flag is still there! I might as well give it to you!

>pwn.college{gmt88ooMBHTpVAJBEGBK6YgqS7g.QX2cDM1wyN5EzNzEzW}
# What I learned
There is a special shell variable, called PATH, that stores a bunch of directory paths in which the shell will search for programs corresponding to commands.
# Reference
None
