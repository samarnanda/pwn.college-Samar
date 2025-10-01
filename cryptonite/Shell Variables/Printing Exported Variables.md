# Printing exported variables
This challenge asks us to execute a command which will print all the exported variables, from which we have to find the "FLAG" variable to get the actual flag.
# My solve
**Flag**-pwn.college{wcAs7ASLseeVKFHK6JkiJJyrYQ_.QX4UTN0wyN5EzNzEzW}

>hacker@variables~printing-exported-variables:~$ env

>SHELL=/run/dojo/bin/bash

>HOSTNAME=variables~printing-exported-variables

>PWD=/home/hacker

>MANPATH=/run/dojo/share/man:

>DOJO_AUTH_TOKEN=68e91e4f72edbeb865d42189fcfe102e7043cbb00a90197410fc6a69906ecd39

>HOME=/home/hacker

>LANG=C.UTF-8

>FLAG=pwn.college{wcAs7ASLseeVKFHK6JkiJJyrYQ_.QX4UTN0wyN5EzNzEzW}

>TERMINFO=/run/dojo/share/terminfo

>TERM=xterm-256color

>SHLVL=2

>LC_CTYPE=C.UTF-8

>SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt

>PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

>DEBIAN_FRONTEND=noninteractive

>_=/run/dojo/bin/env

# What I learned
The "env" command prints all the exported variables.
# Reference
None.
