# Changing Permissions
This challenge asks us to change permissions and make the flag readable for the user using "chmod" command.
# My solve
**Flag**-pwn.college{4CzoteKcvZqNcyUQQMhzJ4Hsyrl.QXzcjM1wyN5EzNzEzW}

>hacker@permissions~changing-permissions:~$ chmod a+r /flag

>hacker@permissions~changing-permissions:~$ cat /flag

>pwn.college{4CzoteKcvZqNcyUQQMhzJ4Hsyrl.QXzcjM1wyN5EzNzEzW}
# What I learned
chmod allows you to tweak permissions with the mode format of WHO+/-WHAT, where WHO is user/group/other and WHAT is read/write/execute.
# Reference 
None
