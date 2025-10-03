# Process exit codes
This challenge asks us to get the exit code of a command and then use that code as an argument to another command to get the flag.
# My solve
**Flag**-pwn.college{0O_vucl83SItpTs21QH2Lb_1FrE.QX5YDO1wyN5EzNzEzW}

>hacker@processes~process-exit-codes:~$ /challenge/get-code

>Exiting with an error code!

>hacker@processes~process-exit-codes:~$ echo $?

>59

>hacker@processes~process-exit-codes:~$ /challenge/submit-code 59

>CORRECT! Here is your flag:

>pwn.college{0O_vucl83SItpTs21QH2Lb_1FrE.QX5YDO1wyN5EzNzEzW}

# What I learned
Every shell command, including every program and every builtin, exits with an exit code when it finishes running and terminates. This can be used by the shell, or the user of the shell to check if the process succeeded in its functionality.
We can access the exit code of the most recently-terminated command using the special ? variable and prepend it with $ to read its value.
Commands that succeed typically return 0 and commands that fail typically return a non-zero value, most commonly 1 but sometimes an error code that identifies a specific failure mode.
# Reference 
None
