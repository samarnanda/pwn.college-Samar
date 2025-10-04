# Changing file ownership
This challenge asks us to change the ownership the file which contains the flag from root to the user (in this case hacker), then read the file to obtain the flag.
# My solve
**Flag**-pwn.college{IbthbjdQu6eWTfy2PWB-Ox1_05F.QXxEjN0wyN5EzNzEzW}

>hacker@permissions~changing-file-ownership:~$ chown hacker /flag

>hacker@permissions~changing-file-ownership:~$ cat /flag

>pwn.college{IbthbjdQu6eWTfy2PWB-Ox1_05F.QXxEjN0wyN5EzNzEzW}

We change the ownership using the "chown" command.

# What I learned
The way we prevent anyone from just invoking a command such as reading the flag file is by having the file owned by the root user, configure its permissions so that no other user can read it. We can change the ownership of files. This is done via the chown (change owner) command.
# Reference
None
