# hidden files
This challenge asks us to find the hidden file which starts from "." using the "ls -a" command to obtain the flag
# My solve
**Flag**- pwn.college{MPWQhiYrlhbDbR6IuTmi2Q_Xhe9.QXwUDO0wyN5EzNzEzW}
 First we change the directory to "/", then we execute "ls -a" command to find the hidden files that start from ".".
 After this we read the hidden . appneded file and obtain the flag

>hacker@commands~hidden-files:~$ cd /

>hacker@commands~hidden-files:/$ ls -a

>.  ..  .dockerenv  .flag-1373782539469  bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var

>hacker@commands~hidden-files:/$ cat .flag-1373782539469

>pwn.college{MPWQhiYrlhbDbR6IuTmi2Q_Xhe9.QXwUDO0wyN5EzNzEzW}

# What I learned
I learned that the ls command does not list the files starting from ".". But we can list them using the command ls -a.
# Reference
None.
