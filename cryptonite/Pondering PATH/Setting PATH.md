# Setting PATH
This challenge asks us to overwrite PATH with a directory which contains the "win" command. But the win command is not in PATH initially. We then need to run a program which needs the win command to print the flag.
# My solve
**Flag**-pwn.college{UuVrZAabXJMc5lwvpuoi-DrNJ5V.QX1cjM1wyN5EzNzEzW}

>hacker@path~setting-path:~$ export PATH=/challenge/more_commands/

>hacker@path~setting-path:~$ /challenge/run

>Invoking 'win'....

>Congratulations! You properly set the flag and 'win' has launched!

>pwn.college{UuVrZAabXJMc5lwvpuoi-DrNJ5V.QX1cjM1wyN5EzNzEzW}

# What I learned
PATH stores a list of directories to find commands in and, for commands in nonstandard places, we must typically execute them via their path.
# Reference
None
