# Position elsewhere
This challenge asks us to execute the command to find the "run" program using the path first. It then asks us to change the directory in which the run program is actually in.
Once we have changed the directory, we execute the path command to find the program and obtain the flag.
# My Solve

**Flag**- pwn.college{EEvZwljpFJ3NzTsB0buk2LaJcNT.QX3QTN0wyN5EzNzEzW}

First we execute the "/challenge/run" command in the terminal. The terminal then tells us that we are not currently in the correct directory in which the program actually is.
The correct directory is "/usr/share/doc/fontconfig". we then use the "cd" command to change the directory by executing "cd /usr/share/doc/fontconfig/".
We then navigate to the program by executing the command "/challenge/run" to obtain the flag.

>hacker@paths~position-elsewhere:~$ /challenge/run

>Incorrect...

>You are not currently in the /usr/share/doc/fontconfig directory.

>Please use the `cd` utility to change directory appropriately.

>hacker@paths~position-elsewhere:~$ cd /usr/share/doc/fontconfig/

>hacker@paths~position-elsewhere:/usr/share/doc/fontconfig$ /challenge/run

>Correct!!!

>/challenge/run is an absolute path, invoked from the right directory!

>Here is your flag:

>pwn.college{EEvZwljpFJ3NzTsB0buk2LaJcNT.QX3QTN0wyN5EzNzEzW}

# What I Learned
I learned that we cannot find a program without first being inside the directory in which the program is in. We use the "cd" command to change directories. The "~" shows the current path where our shell is located at.

# References
None.


