# Writing to multiple programs
This challenge asks us to run a command and then duplicate its output as input to two other commands to obtain the flag.
# My solve
**Flag**-pwn.college{00oZZGn_KObhJS7kRT4eUF3CxtW.QXwgDN1wyN5EzNzEzW}

>hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)

>This secret data must directly and simultaneously make it to /challenge/the and

>/challenge/planet. Don't try to copy-paste it; it changes too fast.

>1814418771869132669

>Congratulations, you have duplicated data into the input of two programs! Here

>is your flag:

>pwn.college{00oZZGn_KObhJS7kRT4eUF3CxtW.QXwgDN1wyN5EzNzEzW}

# What I learned
I learned that bash can make commands look like files using process substitution! For writing to a command (output process substitution), use >(command).
If you write an argument in this form, bash will run the command but hook up its input to a temporary named pipe file. When commands write to this file, the data goes to the standard input of the command.
# Reference
None.
