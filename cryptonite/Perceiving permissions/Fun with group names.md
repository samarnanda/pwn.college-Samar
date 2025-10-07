# Fun with group names
This challenge asks us to figure out the group ourselves using the "id" command and then change group and read flag.
# My solve
**Flag**-pwn.college{w9YZtGshclocUyXLOvK05aGxH0q.QXycjM1wyN5EzNzEzW}

>hacker@permissions~fun-with-groups-names:~$ id

>uid=1000(hacker) gid=1000(grp31008) groups=1000(grp31008)

>hacker@permissions~fun-with-groups-names:~$ chgrp grp31008 /flag

>hacker@permissions~fun-with-groups-names:~$ cat /flag

>pwn.college{w9YZtGshclocUyXLOvK05aGxH0q.QXycjM1wyN5EzNzEzW}

# What I learned
