# moving files
This challenge asks us to move a file from one place to another by using the "mv" command to obtain the flag.
# My solve
**Flag**-pwn.college{MPR1L9o1GF4QdLRmpyoJRCUs5GJ.0VOxEzNxwyN5EzNzEzW}

We invoke the "mv" command and use the file path and the path where we want to move the file, as arguments respectively.
The file path is /flag and the path where we want to move it is /tmp/hack-the-planet.
The full command is: mv /flag /tmp/hack-the-planet

>hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet

>Correct! Performing 'mv /flag /tmp/hack-the-planet'.

>/bin/mv: cannot stat '/flag': No such file or directory

>hacker@commands~moving-files:~$ /challenge/check

>Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:

>pwn.college{MPR1L9o1GF4QdLRmpyoJRCUs5GJ.0VOxEzNxwyN5EzNzEzW}

# What I Learned 
I learned that we can move files from one place to another in Linux using the "mv" command. We use the file name and the place where we want to move it, as arguments respectively.
# Reference
None.
