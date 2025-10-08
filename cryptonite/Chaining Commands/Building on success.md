# Building on success
This challenge asks us to chain two commands using "&&" and get the flag.
# My solve
**Flag**-pwn.college{EuGEIC2wt1d_Jp3dOnsHqwuWfyp.0lM0MDOxwyN5EzNzEzW}

>hacker@chaining~building-on-success:~$ /challenge/first-success

>hacker@chaining~building-on-success:~$ /challenge/second

>Error: /challenge/first-success must be successfully chained with

>/challenge/second using &&

>hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second

>Nice chaining! Flag: pwn.college{EuGEIC2wt1d_Jp3dOnsHqwuWfyp.0lM0MDOxwyN5EzNzEzW}

# What I learned
The && operator allows you to run a second command only if the first command succeeds (in Linux convention, this means it exited with code 0). This is called the "AND" operator because both conditions must be true: the first command must succeed AND then the second command will run.
# Reference
None.
