# Implicit relative paths, from /
This challenge asks navigate a file through just the relative path, without using the aboslute path to obtain the flag. We also need to change the directory to "/" first.
from "/" we will type the relative path into the terminal and obtain the flag by finding the program.
# My solve
**Flag**-pwn.college{EE8uCFrHtA3HULAFTXLZIkFg8cP.QX5QTN0wyN5EzNzEzW}

We first execute "/challenge/run" command, it then tells that we are in the wrong directory and that we need to change our directory to "/". We type "cd /" into the terminal to do this.
After changing the directory, we simply type in "challenge/run" to find the program and obtain the flag. since are currently working directory is "/" and the program is in "/", we dont need to type the absolute path.
We can just type the relative path, which is "challenge/run" and obtain the flag.
>hacker@paths~implicit-relative-paths-from-:~$ /challenge/run

>Incorrect...

>You are not currently in the / directory.

>Please use the `cd` utility to change directory appropriately.

>hacker@paths~implicit-relative-paths-from-:~$ cd /

>hacker@paths~implicit-relative-paths-from-:/$ challenge/run

>Correct!!!

>challenge/run is a relative path, invoked from the right directory!

>Here is your flag:

>pwn.college{EE8uCFrHtA3HULAFTXLZIkFg8cP.QX5QTN0wyN5EzNzEzW}

# What I Learned
I learned that if the file we want to access is in our currently working directory, then we dont need to use the abslute path, we can just type the relative path to find the file.
In this case, the absolute path is "/challenge/run". The relative path does not start with the parent directory, so the relative path is "challenge/run" (without the parent directory "/").
# References 
None.
