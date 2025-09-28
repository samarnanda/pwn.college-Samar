# Matching paths with []
This challenge asks us to obtain the file by using the absolute path as the argument but with [].
# My solve
**Flag**-pwn.college{gZzxf062_iV9bg-rOI8chLttbdP.QX0IDO0wyN5EzNzEzW}

>hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]

>You got it! Here is your flag!

>pwn.college{gZzxf062_iV9bg-rOI8chLttbdP.QX0IDO0wyN5EzNzEzW}

# What I learned
I learned that Globbing happens on a path basis, so we can expand entire paths with our globbed arguments.
# Reference
None.
