# explicit relative paths, from / 
This challenge asks us to explore how "." works. We use "." to run our command to find the file and obtain the flag. We have to run a relative path from the correct directory.
# My solve
**Flag**- pwn.college{cpjyamVpEzARbqILsfEvuet4WAb.QXwUTN0wyN5EzNzEzW}

We first run "/challenge/run" command, the terminal then tells us that we are in the wrong directory and we need to change our directory to "/" using cd.
We then run the relative path "./challenge/run" to obtain the flag. "." takes us to the same directory.

>hacker@paths~explicit-relative-paths-from-:~$ /challenge/run

>Incorrect...

>You are not currently in the / directory.

>Please use the `cd` utility to change directory appropriately.

>hacker@paths~explicit-relative-paths-from-:~$ cd /

>hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run

>Correct!!!

>./challenge/run is a relative path, invoked from the right directory!

>Here is your flag:

>pwn.college{cpjyamVpEzARbqILsfEvuet4WAb.QXwUTN0wyN5EzNzEzW}

# What I learned
I learned that "." is one of the two implicit entries that we can reference in paths. The "." entry refers right to the same directory.
# References
None.
