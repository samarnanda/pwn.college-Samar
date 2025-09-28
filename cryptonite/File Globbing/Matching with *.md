# Matching with *
This challenge asks us to change our directory using the cd command but the argument can have maximum 4 characters. We need to use "*" for this.
# My solve 
**Flag**-pwn.college{cdeHuoIFtsuyoozG3RgXGmoNhJX.QXxIDO0wyN5EzNzEzW}

>hacker@globbing~matching-with-:~$ cd /ch*

>hacker@globbing~matching-with-:/challenge$ /challenge/run

>You ran me with the working directory of /challenge! Here is your flag:

>pwn.college{cdeHuoIFtsuyoozG3RgXGmoNhJX.QXxIDO0wyN5EzNzEzW}

# What I learned
I learned that when it encounters a * character in any argument, the shell will treat it as a "wildcard" and try to replace that argument with any files that match the pattern. The * matches any part of the filename except for / or a leading . character.

# Reference 
None.
