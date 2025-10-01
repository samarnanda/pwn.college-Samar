# Storing command output
This challenge asks us to store the output of a command in a variable and then print that variable in order to obtain the flag.
# My solve
**Flag**-pwn.college{kxU5SmB2UF4jryCZdpn03qdOOFY.QX1cDN1wyN5EzNzEzW}

>hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)

>Congratulations! You have read the flag into the PWN variable. Now print it out

>and submit it!

>hacker@variables~storing-command-output:~$ echo $PWN

>pwn.college{kxU5SmB2UF4jryCZdpn03qdOOFY.QX1cDN1wyN5EzNzEzW}

# What I learned
I learned that we can store the output of a command in a variable by using $().
# Reference
None.
