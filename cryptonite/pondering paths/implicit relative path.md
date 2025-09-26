# implicit relative path
This challenge asks us to use "." to access the file using a relative path as using a naked path gives an error. We run the relative path after changing directory to obtain the flag.
# My solve
We first change our directory to "/challenge". We then try to run a naked path "/challenge/run" but this gives an error, "bash: run: command not found".
We then execute the implicit relative path "./run". This commands finds the "run" program and we obtain the flag.
>hacker@paths~implicit-relative-path:~$ /challenge/run

>Incorrect...

>You are not currently in the /challenge directory.

>Please use the `cd` utility to change directory appropriately.

>hacker@paths~implicit-relative-path:~$ cd /challenge

>hacker@paths~implicit-relative-path:/challenge$ run

>bash: run: command not found

>hacker@paths~implicit-relative-path:/challenge$ ./run

>Correct!!!

>./run is a relative path, invoked from the right directory!

>Here is your flag:

>pwn.college{Uad3gMK_OzqefhHHSM6fDVyMllQ.QXxUTN0wyN5EzNzEzW}
# What I Learned
I learned that Linux explicitly avoids automatically looking in the current directory when you provide a "naked" path. Running the naked path will not actually invoke the program from the directory. his is actually a safety measure: if Linux searched the current directory for programs every time you entered a naked path, you could accidentally execute programs in your current directory that happened to have the same names as core system utilities! As a result, the above commands will yield the following error: bash: run: command not found
# References
None.
