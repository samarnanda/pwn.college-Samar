# Scripting with default cases
This challenge asks write a script that takes one specific argument and gives a specific output for that argument, and gives another output for any argument other than the specific one the challenge (pwn). We do this with the help of "if", "then", "else", "fi".
# My solve
**Flag**-pwn.college{4HGd3YPlZO9uYV6rDPxGHMX1RBZ.01NzMDOxwyN5EzNzEzW}

>hacker@chaining~scripting-with-default-cases:~$ echo '#!/bin/bash' > /home/hacker/solve.sh

>hacker@chaining~scripting-with-default-cases:~$ echo 'if [ "$1" == "pwn" ]' >> /home/hacker/solve.sh

>hacker@chaining~scripting-with-default-cases:~$ echo 'then' >> /home/hacker/solve.sh

>hacker@chaining~scripting-with-default-cases:~$ echo '   echo "college"' >> /home/hacker/solve.sh

>hacker@chaining~scripting-with-default-cases:~$ echo 'else' >> /home/hacker/solve.sh

>hacker@chaining~scripting-with-default-cases:~$ echo '   echo "nope"' >> /home/hacker/solve.sh

>hacker@chaining~scripting-with-default-cases:~$ echo 'fi' >> /home/hacker/solve.sh

>hacker@chaining~scripting-with-default-cases:~$ bash /home/hacker/solve.sh pwn

>college

>hacker@chaining~scripting-with-default-cases:~$ bash /home/hacker/solve.sh foo

>nope

>hacker@chaining~scripting-with-default-cases:~$ bash /home/hacker/solve.sh hack

>nope

>hacker@chaining~scripting-with-default-cases:~$ /challenge/run

>Correct! Your script properly handles the if/else conditions.

>Here's your flag:

>pwn.college{4HGd3YPlZO9uYV6rDPxGHMX1RBZ.01NzMDOxwyN5EzNzEzW}

# What I learned
The else clause executes when the if condition is false.
# Reference
None



pwn.college{4HGd3YPlZO9uYV6rDPxGHMX1RBZ.01NzMDOxwyN5EzNzEzW}

