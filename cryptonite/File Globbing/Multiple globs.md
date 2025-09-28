# Multiple globs
This challenge asks us to obtain the flag by using multiple * globs in a single short (3 characters or less) argument after changing the directory to /challenge/files.
# My solve
**Flag**-pwn.college{UWcTowobbsG2ZAP_qrTtsIu6mEq.0lM3kjNxwyN5EzNzEzW}

>hacker@globbing~multiple-globs:~$ cd /challenge/files

>hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*

>You got it! Here is your flag!

>pwn.college{UWcTowobbsG2ZAP_qrTtsIu6mEq.0lM3kjNxwyN5EzNzEzW}

# What I learned 
I learned that Bash supports the expansion of multiple globs in a single word.
# Reference
None.
