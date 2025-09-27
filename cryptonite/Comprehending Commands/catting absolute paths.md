# catting absolute paths
This challenge asks to read a file by using the "cat" command but this time we have to provide the absolute path of the file as the argument.
# My solve
**Flag**- pwn.college{cmD4s3c53EpnLmyv_ZOYpWQhlog.QX5ETO0wyN5EzNzEzW}

We execute the cat command and provide the absolute path of the "flag" file as argument in order to read the file and obtain the flag. 
The full command would be: cat /flag. The flag file is in the "/" directory.

>hacker@commands~catting-absolute-paths:~$ cat /flag

>pwn.college{cmD4s3c53EpnLmyv_ZOYpWQhlog.QX5ETO0wyN5EzNzEzW}

# What I learned
I learned that we provide the absolute path of a file as the argument in the cat command s well, apart from just the file name.
# Reference 
None.
