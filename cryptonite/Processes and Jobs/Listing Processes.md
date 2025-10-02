# Listing processes
This challenge asks us to find the file which is actually the program needed to find the flag. We find this file using the "ps" command with either "-ef" or "aux" as argument.
# My solve
**Flag**-pwn.college{8fa0UAyZXT5E6AQOPJ2B40aiMep.QX4MDO0wyN5EzNzEzW}

hacker@processes~listing-processes:~$ ps -ef

UID          PID    PPID  C STIME TTY          TIME CMD

root           1       0  0 16:42 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-iroot           7       1  0 16:42 ?        
00:00:00 /run/dojo/bin/sleep 6h

root         132       1  0 16:42 ?        00:00:00 /challenge/25478-run-11006

root         135     132  0 16:42 ?        00:00:00 sleep 6h

hacker       146       1  0 16:42 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --pohacker       150     146  0 16:43 pts/0    
00:00:00 /run/dojo/bin/bash --login

hacker       160       0  0 16:43 pts/1    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/hacker       166     160  0 16:43 pts/1    
00:00:00 /run/dojo/bin/bash --login

hacker       175     166  0 16:44 pts/1    00:00:00 ps -ef

hacker@processes~listing-processes:~$ ps aux

USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND

root           1  0.0  0.0   1056   640 ?        Ss   16:42   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-worksroot           7  0.0  0.0 231708  2560 ?   
S    16:42   0:00 /run/dojo/bin/sleep 6h

root         132  0.0  0.0   4132  2560 ?        S    16:42   0:00 /challenge/25478-run-11006

root         135  0.0  0.0   2744  1600 ?        S    16:42   0:00 sleep 6h

hacker       146  0.0  0.0  36972 21760 ?        Sl   16:42   0:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.hacker       150  0.0  0.0 231940  4160 
pts/0    Ss+  16:43   0:00 /run/dojo/bin/bash --login

hacker       160  0.0  0.0 231576  3520 pts/1    Ss   16:43   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-intehacker       166  0.0  0.0 231940  4160 
pts/1    S    16:43   0:00 /run/dojo/bin/bash --login

hacker       176  0.0  0.0 233600  3840 pts/1    R+   16:44   0:00 ps aux

hacker@processes~listing-processes:~$ /challenge/25478-run-11006

Yahaha, you found me! Here is your flag:

pwn.college{8fa0UAyZXT5E6AQOPJ2B40aiMep.QX4MDO0wyN5EzNzEzW}

Now I will sleep for a while (so that you could find me with 'ps').

# What I learned
I learnt to list running processes using the ps command. Ech process has a numerical identifier (the Process ID, or PID), which is a number that uniquely identifies every running process in a Linux environment. We also see the terminal on which the commands are running (in this case, the designation pts/0), and the total amount of cpu time that the process has eaten up so far.

# Reference
None.


