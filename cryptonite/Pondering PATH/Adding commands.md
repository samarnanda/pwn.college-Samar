# Adding commands
This challenge asks us to create an executable shell script named win in a new directory that uses the absolute path /run/dojo/bin/cat (or the built-in read) to print /flag, then overwrite our PATH to point only at that directory so /challenge/run finds and executes our win script.
# My solve
**Flag**-pwn.college{QGxqeebJcod08Gcu6U_hHbBbrgV.QX2cjM1wyN5EzNzEzW}

>hacker@path~adding-commands:~$ which cat

>/run/dojo/bin/cat

>hacker@path~adding-commands:~$ mkdir ~/scripts

>mkdir: cannot create directory ‘/home/hacker/scripts’: File exists

>hacker@path~adding-commands:~$ which cat

>/run/dojo/bin/cat

>hacker@path~adding-commands:~$ mkdir ~/myscripts

>hacker@path~adding-commands:~$ cd ~/my

>myflag     myscripts/

>hacker@path~adding-commands:~$ cd ~/myscripts

>hacker@path~adding-commands:~/myscripts$ echo '#!/bin/bash' > win

>hacker@path~adding-commands:~/myscripts$ echo '/run/dojo/bin/cat /flag' >> win

>hacker@path~adding-commands:~/myscripts$ chmod a+x win

>hacker@path~adding-commands:~/myscripts$ export PATH=~/myscripts

>hacker@path~adding-commands:~/myscripts$ /challenge/run

>Invoking 'win'....

>pwn.college{QGxqeebJcod08Gcu6U_hHbBbrgV.QX2cjM1wyN5EzNzEzW}

# References
None
