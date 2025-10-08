# Scripting with conditionals
This challenge asks us to take an argument and according to the condition we have to give the output. For this we use "if", "then" etc. and the terminator of the if statement is "fi".
# My solve
**Flag**-pwn.college{kHz1TJlFJYZ72JwseFQUX_1r9Ik.0lNzMDOxwyN5EzNzEzW}

>hacker@chaining~scripting-with-conditionals:~$ bash /home/hacker/solve.sh pwn

>hacker@chaining~scripting-with-conditionals:~$ echo '#!/bin/bash' > /home/hacker/solve.sh

>hacker@chaining~scripting-with-conditionals:~$ echo 'if [ "$1" == "pwn" ]' >> /home/hacker/solve.sh

>hacker@chaining~scripting-with-conditionals:~$ echo 'then' >> /home/hacker/solve.sh

>hacker@chaining~scripting-with-conditionals:~$ echo '   echo "college"' >> /home/hacker/solve.sh

>hacker@chaining~scripting-with-conditionals:~$ echo 'fi' >> /home/hacker/solve.sh

>hacker@chaining~scripting-with-conditionals:~$ bash /home/hacker/solve.sh pwn

>college

>hacker@chaining~scripting-with-conditionals:~$ bash /home/hacker/solve.sh foo

>hacker@chaining~scripting-with-conditionals:~$ /challenge/run

>Correct! Your script properly handles all the conditions.

>Here's your flag:

>pwn.college{kHz1TJlFJYZ72JwseFQUX_1r9Ik.0lNzMDOxwyN5EzNzEzW}

# Reference
None.
