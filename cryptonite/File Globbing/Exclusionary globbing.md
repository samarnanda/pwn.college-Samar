# Exclusionary globbing
This challenge asks us to run all the files that do NOT start with "p", "w", or "n". We achieve this with the help of ! inside [] to obtain the flag
# My solve
**Flag**-

>hacker@globbing~exclusionary-globbing:~$ cd /challenge/files

>hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*

>You got it! Here is your flag!

>pwn.college{Y5NcAwIsz31q2LaAZIWnCYlg-WA.QX2IDO0wyN5EzNzEzW}

# What I learned
I learned that we can also filter out files in a directory using either ! or * with []
# Reference 
None.
