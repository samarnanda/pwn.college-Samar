# Duplicating piped data with tee
This challenge asks us to duplicate the output of the program to a file and then read the file in order to execute the entire command successfully, using "tee".
# My solve
**Flag**-pwn.college{sVBrThRGY5f1nHZ1gwRmYxBFJO0.QXxITO0wyN5EzNzEzW}

hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee output | /challenge/college
Processing...
WARNING: you are overwriting file output with tee's output...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat output
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "sVBrThRG"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret sVBrThRG | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{sVBrThRGY5f1nHZ1gwRmYxBFJO0.QXxITO0wyN5EzNzEzW}

# Reference
None.
