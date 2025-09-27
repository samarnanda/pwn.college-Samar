# linking files
This challenge teaches us how to link files using the "ln -s" command and the file/directory as argument.
# My solve 
**Flag**- pwn.college{cr46p1ZGdb8m5hJDjoNv4svaY_r.QX5ETN1wyN5EzNzEzW}

>hacker@commands~linking-files:~$ /challenge/catflag

>About to read out the /home/hacker/not-the-flag file!

>cat: /home/hacker/not-the-flag: No such file or directory

>hacker@commands~linking-files:~$ ln -s /flag ~/not-the-flag

>hacker@commands~linking-files:~$ /challenge/catflag

>About to read out the /home/hacker/not-the-flag file!

>pwn.college{cr46p1ZGdb8m5hJDjoNv4svaY_r.QX5ETN1wyN5EzNzEzW}

# References
None.
