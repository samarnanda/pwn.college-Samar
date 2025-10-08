# Scripting with arguments
This challenge asks us to write a script that takes two arguments and outputs them in the reverse order. Once this script functions properly we run another program to obtain the flag.
# My solve
**Flag**-pwn.college{oHh1SErlW7YiYOUelVtdDwrgeOV.0VNzMDOxwyN5EzNzEzW}

>hacker@chaining~scripting-with-arguments:~$ echo '#!/bin/bash' > /home/hacker/solve.sh

>hacker@chaining~scripting-with-arguments:~$ echo 'echo $2 $1' >> /home/hacker/solve.sh

>hacker@chaining~scripting-with-arguments:~$ bash /home/hacker/solve.sh pwn college

>college pwn

>hacker@chaining~scripting-with-arguments:~$ /challenge/run

>Correct! Your script properly reversed the arguments.

>Here's your flag:

>pwn.college{oHh1SErlW7YiYOUelVtdDwrgeOV.0VNzMDOxwyN5EzNzEzW}
# What I learned
The script can access the arguments using special variables:

$1 contains the first argument ("hello")

$2 contains the second argument ("world")

$3 would contain the third argument (if there had been one)

...and so on
# Reference
None
