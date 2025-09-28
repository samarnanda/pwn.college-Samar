# Helpful Programs
This challenge asks us to read a program's documentation using "--help" as the argument.
# My solve 
**Flag**-pwn.college{UttiCDG-DM3Ge9o2SRM-XSwi-TR.QX3IDO0wyN5EzNzEzW}

hacker@man~helpful-programs:~$ --help

bash: --help: command not found

hacker@man~helpful-programs:~$ man challenge

No manual entry for challenge

hacker@man~helpful-programs:~$ -h

bash: -h: command not found

hacker@man~helpful-programs:~$ /challenge/challenge --help

usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:

-h, --help            show this help message and exit

--fortune             read your fortune

-v, --version         get the version number

-g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG

get the flag, if given the correct value

-p, --print-value     print the value that will cause the -g option to give you the flag

hacker@man~helpful-programs:~$ /challenge/challenge -g

usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

a challenge to make you ask for help: error: argument -g/--give-the-flag: expected one argument

hacker@man~helpful-programs:~$ /challenge/challenge -g/--give-the-flag

usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: '/--give-the-flag'

hacker@man~helpful-programs:~$ /challenge/challenge -p

The secret value is: 392

hacker@man~helpful-programs:~$ /challenge/challenge -g/392

usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: '/392'

hacker@man~helpful-programs:~$ /challenge/challenge -g392

Correct usage! Your flag: pwn.college{UttiCDG-DM3Ge9o2SRM-XSwi-TR.QX3IDO0wyN5EzNzEzW}

# References 
None.
