# Executable shell scripts
This challenge asks us to make a script with a program and make that script executable so that we can invoke the script without bash and just via the relative or the absolute path.
# My solve
**Flag**-pwn.college{gwQe2qTM7LZzBU1oLUZrjXAczOn.QX0cjM1wyN5EzNzEzW}

>hacker@chaining~executable-shell-scripts:~$ echo /challenge/solve > script.sh

>hacker@chaining~executable-shell-scripts:~$ chmod a+x script.sh

>hacker@chaining~executable-shell-scripts:~$ ./script.sh

>Congratulations on your shell script execution! Your flag:

>pwn.college{gwQe2qTM7LZzBU1oLUZrjXAczOn.QX0cjM1wyN5EzNzEzW}

# What I learned
If we make a script executable for all by using chmod we can invoke the script just by its path without the need of bash.
# Reference
None
