# Redirecting script output
This challenge asks us to create a script which contains programs which we need to pipe using "|" to another program. This will finally give us the flag.
# My solve
**Flag**-pwn.college{4QG5LQFvGyN8mrcCB88pT_UoRWR.QX4ETO0wyN5EzNzEzW}

>hacker@chaining~redirecting-script-output:~$ echo /challenge/pwn > script.sh

>hacker@chaining~redirecting-script-output:~$ echo /challenge/college >> script.sh

>hacker@chaining~redirecting-script-output:~$ bash script.sh | /challenge/solve

>Correct! Here is your flag:

>pwn.college{4QG5LQFvGyN8mrcCB88pT_UoRWR.QX4ETO0wyN5EzNzEzW}

# What I learned
If we want to send the output of several programs to one command we can do this by redirecting output from our script.
All of the various redirection methods work: > for stdout, 2> for stderr, < for stdin, >> and 2>> for append-mode redirection, >& for redirecting to other file descriptors, and | for piping to another command.

# Reference
None
