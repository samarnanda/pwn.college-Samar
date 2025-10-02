# Deleting characters
This challenge asks us to delete certain characters from the flag in order to get the correct flag by using "-d" as argument for "tr".
# My solve
**Flag**-pwn.college{815TUyR6nBBs0vJoIotUQz814Ie.0FNxEzNxwyN5EzNzEzW}

>hacker@data~deleting-characters:~$ /challenge/run | tr -d '^%'

>Your character-stuffed flag:

>pwn.college{815TUyR6nBBs0vJoIotUQz814Ie.0FNxEzNxwyN5EzNzEzW}

# What I learned
tr can also translate characters to nothing (i.e., delete them). This is done via a -d flag and an argument of what characters to delete.
# Reference
None.
