# touching files
This challenge asks us to create files in a directory using the "touch" command. Also to list these files from the dirctory using the ls command.
# My solve
Since we have to create files in the "/tmp" directory, we change the directory to /tmp through "cd /tmp".
We then use the ls command to confirm that are directory doesnt have these files already. We then create the files using the "touch" command.
"touch pwn" and "touch college" commands create the pwn and the college files in the /tmp directory.
We then run /challenge/run to obtain the flag.

>hacker@commands~touching-files:~$ cd /tmp

>hacker@commands~touching-files:/tmp$ ls

>bin  hsperfdata_root  tmp.4mK6TfTSUV

>hacker@commands~touching-files:/tmp$ touch pwn

>hacker@commands~touching-files:/tmp$ ls

>bin  hsperfdata_root  pwn  tmp.4mK6TfTSUV

>hacker@commands~touching-files:/tmp$ touch college

>hacker@commands~touching-files:/tmp$ ls

>bin  college  hsperfdata_root  pwn  tmp.4mK6TfTSUV

>hacker@commands~touching-files:/tmp$ /challenge/run

>Success! Here is your flag:

>pwn.college{8f3fDSF-Sjmfsv0xy6xcevJrKFH.QXwMDO0wyN5EzNzEzW}

# What I learned
I learned that we can always create files inside a directory using the "touch" command. If we are already in the directory, then we just use the name of the file as the argument. We can also use the absolute paths as the argument if we have not changed directories.
# References 
None.

