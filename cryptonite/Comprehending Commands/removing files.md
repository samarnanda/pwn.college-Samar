# removing files
This challenge asks us to remove files from the directory using the "rm" command.
# My solve
**Flag**- pwn.college{INjm5CWE0H52UeyY93bxJPUilc6.QX2kDM1wyN5EzNzEzW}
We first create a "delete_me" file using the touch command and then list the files of the directory using ls command.
We then delete the file from the directory using the "rm" command.
The full command is: rm delete_me

>hacker@commands~removing-files:~$ touch delete_me

>hacker@commands~removing-files:~$ ls

>Desktop  delete_me  f

>hacker@commands~removing-files:~$ rm delete_me

>hacker@commands~removing-files:~$ ls

>Desktop  f

>hacker@commands~removing-files:~$ /challenge/check

>Excellent removal. Here is your reward:

>pwn.college{INjm5CWE0H52UeyY93bxJPUilc6.QX2kDM1wyN5EzNzEzW}

# What I learned
I learned that we can also delete files from the directory using the "rm" command. We can use the file name or the path as the argument.
# References
None.
