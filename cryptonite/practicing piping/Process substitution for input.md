# Process substitution for input
This challenge asks us to diff two sets of command outputs: /challenge/print_decoys, which will print a bunch of decoy flags, and /challenge/print_decoys_and_flag which will print those same decoys plus the real flag. We will do this by process substitution.
# My solve
**Flag**-pwn.college{ooAfjfoknuKHAYI1z7Z2Ua7Ls-9.0lNwMDOxwyN5EzNzEzW}

>hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
>39a40
> > pwn.college{ooAfjfoknuKHAYI1z7Z2Ua7Ls-9.0lNwMDOxwyN5EzNzEzW}

# What I learned
Linux follows the philosophy that "everything is a file". That is, the system strives to provide file-like access to most resources, including the input and output of running programs! The shell follows this philosophy, allowing you to, for example, use any utility that takes file arguments on the command line and hook it up to the output of programs.

# Reference
None.
