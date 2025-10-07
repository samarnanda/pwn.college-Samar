# Groups and files
This challenge asks us to change our current group (root) ownership to the group owner which can access the flag (hacker) by using the "chgroup" (change group) command, and then read the flag.
# My solve
**Flag**-pwn.college{kv1EDwU9AlR2AlPVUmL2DPZUIDY.QXxcjM1wyN5EzNzEzW}

>hacker@permissions~groups-and-files:~$ chgrp hacker /flag

>hacker@permissions~groups-and-files:~$ cat /flag

>pwn.college{kv1EDwU9AlR2AlPVUmL2DPZUIDY.QXxcjM1wyN5EzNzEzW}

# What I learned
