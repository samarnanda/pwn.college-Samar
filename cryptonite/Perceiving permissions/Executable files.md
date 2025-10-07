# Executable files
This challenge asks us to change permissions using "chmod" and make the program executable. We then run the program to get the flag.
# My solve
**Flag**-pwn.college{UfPfh18c6LUpLv2-fSFymVPHiGQ.QXyEjN0wyN5EzNzEzW}

>hacker@permissions~executable-files:~$ chmod a+x /challenge/run

>hacker@permissions~executable-files:~$ /challenge/run

>Successful execution! Here is your flag:

>pwn.college{UfPfh18c6LUpLv2-fSFymVPHiGQ.QXyEjN0wyN5EzNzEzW}

# What I learned
When you invoke a program, Linux will only actually execute it if you have execute-access to the program file.
# Reference 
None
