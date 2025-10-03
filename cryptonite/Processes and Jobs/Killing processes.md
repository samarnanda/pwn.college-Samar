# Killing Processes 
This challenge asks us to kill a program first, as "/challenge/run" wont run as long as that program is running. After killing the program we run /challenge/run to obtain the flag.
# My solve
**Flag**-pwn.college{sJsd27WFztqfdw1TXXzLSMPXxeo.QXyQDO0wyN5EzNzEzW}

>hacker@processes~killing-processes:~$ ps -e | grep sleep

> 137 ?        00:00:00 sleep

>hacker@processes~killing-processes:~$ kill 137
 
>hacker@processes~killing-processes:~$ /challenge/run
 
>Great job! Here is your payment:
 
>pwn.college{sJsd27WFztqfdw1TXXzLSMPXxeo.QXyQDO0wyN5EzNzEzW}

# What I learned
kill will terminate a process in a way that gives it a chance to get its affairs in order before ceasing to exist.
sleep is a program that simply hangs out for the number of seconds specified on the commandline.

# Reference 
None.
