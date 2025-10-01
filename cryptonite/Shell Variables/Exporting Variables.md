# Exporting Variables
This challenge asks us to set a variable with a value and export it, set another variable with a value but not to export it and then run the program /challenge/run to obtain the flag.
# My solve
**Flag**-pwn.college{YJwBdIZFe_DQkuAgEBsO0izYgtB.QXyYTN0wyN5EzNzEzW}

>hacker@variables~exporting-variables:~$ export PWN=COLLEGE

>You've set the PWN variable to the proper value!

>hacker@variables~exporting-variables:~$ COLLEGE=PWN

>You've set the PWN variable to the proper value!

>You've set the COLLEGE variable to the proper value!

>hacker@variables~exporting-variables:~$ /challenge/run

>CORRECT!

>You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great

>job! Here is your flag:

>pwn.college{YJwBdIZFe_DQkuAgEBsO0izYgtB.QXyYTN0wyN5EzNzEzW}

>You've set the PWN variable to the proper value!

>You've set the COLLEGE variable to the proper value!

# What I learned
By default, variables that you set in a shell session are local to that shell process. That is, other commands you run won't inherit them.
The $ prompt is the prompt of sh, a minimal shell implementation that is invoked as a child of the main shell process.
When you export your variables, they are passed into the environment variables of child processes.
# Reference
None.
