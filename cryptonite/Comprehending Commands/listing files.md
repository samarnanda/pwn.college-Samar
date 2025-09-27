# listing files
This challenge asks us find the "run" program which has been renamed, with the help of "ls" command to list all the files in the directory.
# My solve 
**Flag**- pwn.college{8GqiGsHI-8HXbhboFXfWgNC9A2h.QX4IDO0wyN5EzNzEzW}

First we execute the "ls /challenge" command. This shows us all the files which are in the /challenge directory. The renamed "run" program is also in the /challenge directory.
The new name is: 5672-renamed-run-18974. So we run the program with the command: /challenge/5672-renamed-run-18974, and obtain the flag.

>hacker@commands~listing-files:~$ ls /challenge

>5672-renamed-run-18974  DESCRIPTION.md

>hacker@commands~listing-files:~$ cat /challenge/5672-renamed-run-18974

>#!/opt/pwn.college/bash


>echo "Yahaha, you found me! Here is your flag:"

>cat /flag

>hacker@commands~listing-files:~$ cat /flag

>cat: /flag: Permission denied

>hacker@commands~listing-files:~$ echo "Yahaha, you found me! Here is your flag:"

>Yahaha, you found me! Here is your flag:

>hacker@commands~listing-files:~$ /challenge/5672-renamed-run-18974

>Yahaha, you found me! Here is your flag:

>pwn.college{8GqiGsHI-8HXbhboFXfWgNC9A2h.QX4IDO0wyN5EzNzEzW}

# What I learned
I learned that we can list all the files in a particular directory by using ls command and the directory name as the argument.
If no arguments are provided then the ls command shows everything which is in the home directory.

# References
None.
