# Maching with []
This challenge asks us to obtain the flag by using [] in arguments to run certain files which are already in the /challenge/files directory
# My solve
**Flag**-pwn.college{8_ISB79GvRi3SwBNHRzD6fQyHNg.QXzIDO0wyN5EzNzEzW}

>hacker@globbing~matching-with-:~$ cd /challenge/files

>hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]

>You got it! Here is your flag!

>pwn.college{8_ISB79GvRi3SwBNHRzD6fQyHNg.QXzIDO0wyN5EzNzEzW}

# What I learned
I learned that the square brackets are, essentially, a limited form of ?, in that instead of matching any character, [] is a wildcard for some subset of potential characters, specified within the brackets.
# Reference
None.
