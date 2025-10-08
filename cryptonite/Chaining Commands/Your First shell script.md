# First Shell script
This challenge asks us to create a shell script which consists of programs which we need to run using bash in order to obtain the flag.
# My solve
**Flag**-pwn.college{4ffAjeVmeEnIJIBU_GP1CQV9yN7.QXxcDO0wyN5EzNzEzW}

>hacker@chaining~your-first-shell-script:~$ echo /challenge/pwn > x.sh

>hacker@chaining~your-first-shell-script:~$ echo /challenge/college >> x.sh

>hacker@chaining~your-first-shell-script:~$ bash x.sh

>Great job, you've written your first shell script! Here is the flag:

>pwn.college{4ffAjeVmeEnIJIBU_GP1CQV9yN7.QXxcDO0wyN5EzNzEzW}

# What I learned
As we combine more and more commands to achieve complex effects, the length of the combined prompt quickly gets really annoying to deal with. When this happens, we can put these commands in a file, called a shell script, and run them by executing the file. By convention, shell scripts are frequently named with a sh suffix.
# Reference
None
