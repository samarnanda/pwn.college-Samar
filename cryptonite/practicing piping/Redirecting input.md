# Redirecting input
This challenge asks us to redirect the output of "echo COLLEGE" to a file called PWN and then redirecting the file to /challenge/run.
# My solve
**Flag**-pwn.college{8WNzi5jy1UtDiS8A5dBQ4py7-oX.QXwcTN0wyN5EzNzEzW}

>hacker@piping~redirecting-input:~$ echo COLLEGE > PWN

>hacker@piping~redirecting-input:~$ cat PWN

>COLLEGE

>hacker@piping~redirecting-input:~$ /challenge/run < PWN

>Reading from standard input...

>Correct! You have redirected the PWN file into my standard input, and I read

>the value 'COLLEGE' out of it!

>Here is your flag:

>pwn.college{8WNzi5jy1UtDiS8A5dBQ4py7-oX.QXwcTN0wyN5EzNzEzW}

# What I learned
I learned that just like you can redirect output from programs, you can redirect input to programs! This is done using <.
# Reference
None.
