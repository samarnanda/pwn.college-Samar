# Reading Shell Scripts
This challenge asks us to read a  shell script and figure out the password which is required to get the flag when we run /challenge/run. We use "cat" to read the script.
# My solve
**Flag**-pwn.college{E-g-RSxjSenrHhwnHpTPK5oCRam.0lMwgDOxwyN5EzNzEzW}

>hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run

>Correct! Your script properly handles all the conditions with elif.

>Here's your flag:

>pwn.college{QT3dSBLmTDA0-9X3NlbWMCd105N.0FOzMDOxwyN5EzNzEzW}

>hacker@chaining~scripting-with-multiple-conditions:~$

>Connected!

>hacker@chaining~reading-shell-scripts:~$ cat /challenge/run

>#!/opt/pwn.college/bash


>read GUESS

>if [ "$GUESS" == "hack the PLANET" ]

>then

>    echo "CORRECT! Your flag:"
        
>    cat /flag

>else

>    echo "Read the /challenge/run file to figure out the correct password!"

>fi

>hacker@chaining~reading-shell-scripts:~$ /challenge/run

>hack the PLANET

>CORRECT! Your flag:

>pwn.college{E-g-RSxjSenrHhwnHpTPK5oCRam.0lMwgDOxwyN5EzNzEzW}

# Reference
None
