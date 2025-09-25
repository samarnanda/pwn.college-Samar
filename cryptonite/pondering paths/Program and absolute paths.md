# Program and absolute paths
This challenge asks us to find the "run" program which is in the "challenge" directory and the "challenge" directory is in the "/" directory.
Once we find the "run" program, we obtain the flag.
# My Solve
**Flag**- pwn.college{M2wnRVaeBdiiCgLti4JHjUir28-.QX1QTN0wyN5EzNzEzW}

We type the absolute path to the run program into the command line. The path to the "challenge" directory which is in the "/" directory is "/challenge".Thus, the absolute path to the "run" program which is in the challenge directory is "/challenge/run".

>hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{M2wnRVaeBdiiCgLti4JHjUir28-.QX1QTN0wyN5EzNzEzW}

# What I learned
I learned that, in order to find a program or directory which lives inside another directory, we use "/" to access it from the directory in which the respective program or directory lives.

# References
None.
