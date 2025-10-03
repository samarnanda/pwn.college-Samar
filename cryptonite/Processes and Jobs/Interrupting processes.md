# Interrupting processes
This challenge asks us to run a program and then "interrupt" it using ctrl-c to obtain the flag.
# My solve
**Flag**-pwn.college{AGqnuhqCvCBVfxnVtFIv4i0R-SP.QXzQDO0wyN5EzNzEzW}

>hacker@processes~interrupting-processes:~$ /challenge/run

>I could give you the flag... but I won't, until this process exits. Remember,

>you can force me to exit with Ctrl-C. Try it now!

>^C

>Good job! You have used Ctrl-C to interrupt this process! Here is your flag:

>pwn.college{AGqnuhqCvCBVfxnVtFIv4i0R-SP.QXzQDO0wyN5EzNzEzW}

# What I learned
Terminals have a hotkey for this: Ctrl-C (e.g., holding down the Ctrl key and pressing C) sends an "interrupt" to whatever application is waiting on input from the terminal and, typically, this causes the application to cleanly exit.
# Reference
None.
