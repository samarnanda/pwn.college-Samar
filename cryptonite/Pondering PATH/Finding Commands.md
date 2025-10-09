# Finding Commands
This challenge asks us to find in which directory the "win" command is. The flag is in the same directory and we have to read it using "cat".
# My solve
**Flag**-pwn.college{wgwSAJ-3UJNsHjOf8h0ZsBQJeMm.01NzEzNxwyN5EzNzEzW}

>hacker@path~finding-commands:~$ which win

>/challenge/paths/19390/win

>hacker@path~finding-commands:~$ cat /challenge/paths/19390/flag

>pwn.college{wgwSAJ-3UJNsHjOf8h0ZsBQJeMm.01NzEzNxwyN5EzNzEzW}

# What I learned
Mirroring what the shell does when searching for commands, which looks at each directory in $PATH in order and prints the first file it finds whose name matches the argument we passed.
# Reference
None
