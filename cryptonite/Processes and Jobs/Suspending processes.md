# Suspending processes
This challenge asks us to run the program, suspend it and then run a copy of this program while the original is suspended, to obtain the flag
# My solve
**Flag**-pwn.college{ET5XF5TdJ5Z18OzQulAj6CDORTA.QX1QDO0wyN5EzNzEzW}

>hacker@processes~suspending-processes:~$ /challenge/run
>I'll only give you the flag if there's already another copy of me running in
>this terminal... Let's check!

>UID          PID    PPID  C STIME TTY          TIME CMD
>root         161     152  0 17:58 pts/1    00:00:00 bash /challenge/run
>root         163     161  0 17:58 pts/1    00:00:00 ps -f

>I don't see a second me!

>To pass this level, you need to suspend me and launch me again! You can
>background me with Ctrl-Z or, if you're not ready to do that for whatever
>reason, just hit Enter and I'll exit!
>^Z
>[1]+  Stopped                 /challenge/run
>hacker@processes~suspending-processes:~$ /challenge/run
>I'll only give you the flag if there's already another copy of me running in
>this terminal... Let's check!

>UID          PID    PPID  C STIME TTY          TIME CMD
>root         161     152  0 17:58 pts/1    00:00:00 bash /challenge/run
>root         168     152  0 17:58 pts/1    00:00:00 bash /challenge/run
>root         170     168  0 17:58 pts/1    00:00:00 ps -f

>Yay, I found another version of me! Here is the flag:
>pwn.college{ET5XF5TdJ5Z18OzQulAj6CDORTA.QX1QDO0wyN5EzNzEzW}

# What I learned
I learned that we can suspend processes to the background with Ctrl-Z.
# Reference
None.
