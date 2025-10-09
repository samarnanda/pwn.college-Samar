# Reading Shell Scripts
This challenge asks us to read a  shell script and figure out the password which is required to get the flag when we run /challenge/run. We use "cat" to read the script.
# My solve
**Flag**-pwn.college{E-g-RSxjSenrHhwnHpTPK5oCRam.0lMwgDOxwyN5EzNzEzW}

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
