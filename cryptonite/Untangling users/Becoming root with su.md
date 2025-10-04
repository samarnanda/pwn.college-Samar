# Becoming root with su
This challenge asks us to provide the root password to su to become the root and then read the flag.
# My solve
**Flag**-pwn.college{Y5ilM3fvtUidrBi9GdqPdNzZVqu.QX1UDN1wyN5EzNzEzW}

>hacker@users~becoming-root-with-su:~$ su

>Password:

>root@users~becoming-root-with-su:/home/hacker# cat flag

>cat: flag: No such file or directory

>root@users~becoming-root-with-su:/home/hacker# cat /flag

>pwn.college{Y5ilM3fvtUidrBi9GdqPdNzZVqu.QX1UDN1wyN5EzNzEzW}

# What I learned
Because it has the SUID bit set, su runs as root. Running as root, it can start a root shell.
Before allowing the user to elevate privileges to root, it checks to make sure that the user knows the root password.
# Reference
None
