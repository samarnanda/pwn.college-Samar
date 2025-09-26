# Position thy self
This challenge asks us to navigate to a program by changing directories. We use the "cd" command to change directories. 
# My Solve
**Flag**- pwn.college{U10cdzF2nWT4TwuYvJe9KV-xEWD.QX2QTN0wyN5EzNzEzW}

First, we rerun the previous command which was "/challenge/run", then the terminal tells us that the run program is in a different directory and we need to change our directory to the /usr/include directory. To do that we execute the "cd usr/include/" command. Now the directory has changed and we can find the "run" program by givng the command "/challenge/run" to obtain the flag.

>hacker@paths~position-thy-self:~$ /challenge/run

>Incorrect...

>You are not currently in the /usr/include directory.

>Please use the `cd` utility to change directory appropriately.

>hacker@paths~position-thy-self:~$ cd /usr/include/

>hacker@paths~position-thy-self:/usr/include$ /challenge/run

>Correct!!!

>/challenge/run is an absolute path, invoked from the right directory!

>Here is your flag:

>pwn.college{U10cdzF2nWT4TwuYvJe9KV-xEWD.QX2QTN0wyN5EzNzEzW}

# What I learned
I learned that we cannot find a program without first being inside the directory in which the program is in. We use the "cd" command to change directories. The "~" shows the current path where our shell is located at.

# References 
None.
