# Other users with su
This challenge asks us to switch to a different user zardus, provide the password and then run the program to obtain the flag.
# My solve
**Flag**-pwn.college{M0l1LSUSyb06Sp8nTcEPygF_-E1.QX2UDN1wyN5EzNzEzW}

>hacker@users~other-users-with-su:~$ su zardus

>Password:

>zardus@users~other-users-with-su:/home/hacker$ /challenge/run

>Congratulations, you have become Zardus! Here is your flag:

>pwn.college{M0l1LSUSyb06Sp8nTcEPygF_-E1.QX2UDN1wyN5EzNzEzW}

# What I learned
With no arguments, su will start a root shell (after authenticating with root's password). However, we can also give a username as an argument to switch to that user instead of root.
# Reference
None
