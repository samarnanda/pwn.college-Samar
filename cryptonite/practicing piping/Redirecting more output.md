# Redirecting more output
This challenge asks us to run a command and then redirect the ouput of that command into a file and then read that file to finally obtain the flag.
# My solve
**Flag**-pwn.college{IvWX6JdHOu5WW8kGp1Oie-DtnIa.QX1YTN0wyN5EzNzEzW}

hacker@piping~redirecting-more-output:~$ /challenge/run > myflag

[INFO] WELCOME! This challenge makes the following asks of you:

[INFO] - the challenge will check that output is redirected to a specific file path : myflag

[INFO] - the challenge will output a reward file if all the tests pass : /flag


[HYPE] ONWARDS TO GREATNESS!


[INFO] This challenge will perform a bunch of checks.

[INFO] If you pass these checks, you will receive the /flag file.


[TEST] You should have redirected my stdout to a file called myflag. Checking...


[PASS] The file at the other end of my stdout looks okay!

[PASS] Success! You have satisfied all execution requirements.

hacker@piping~redirecting-more-output:~$ cat myflag


[FLAG] Here is your flag:

[FLAG] pwn.college{IvWX6JdHOu5WW8kGp1Oie-DtnIa.QX1YTN0wyN5EzNzEzW}

# What I learned
I learned that we can redirect the output of a command into another file using ">".

# Reference 
None.
