# Using sudo
This challenge asks us to use sudo with our command to read the flag so that we can get permission and get the flag.
# My solve
**Flag**-pwn.college{sSzSmnJwYEI0bmimcpkmarf82nK.QX4UDN1wyN5EzNzEzW}

>hacker@users~using-sudo:~$ cat /flag

>cat: /flag: Permission denied

>hacker@users~using-sudo:~$ sudo cat /flag

>pwn.college{sSzSmnJwYEI0bmimcpkmarf82nK.QX4UDN1wyN5EzNzEzW}

# What I learned
Unlike su, which relies on password authentication, sudo checks policies to determine whether the user is authorized to run commands as root. 

# Reference
None
