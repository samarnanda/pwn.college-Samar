# The SUID Bit
This challenge asks us to add the SUID Bit to a program in order to spawn a root shell so that we can "cat" the flag ourselves.
# My solve
**Flag**-pwn.college{A9uZVz9Cmyqh65tGjkLIXJlIgSC.QXzEjN0wyN5EzNzEzW}

>hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot

>hacker@permissions~the-suid-bit:~$ /challenge/getroot

>SUCCESS! You have set the suid bit on this program, and it is running as root!

>Here is your shell...

>root@permissions~the-suid-bit:~# cat /flag

>pwn.college{A9uZVz9Cmyqh65tGjkLIXJlIgSC.QXzEjN0wyN5EzNzEzW}

# What I learned
The "Set User ID" (SUID) permissions bit allows the user to run a program as the owner of that program's file.
The s part in place of the executable bit means that the program is executable with SUID. It means that, regardless of what user runs the program (as long as they have executable permissions), the program will execute as the owner user.
# Reference
None
