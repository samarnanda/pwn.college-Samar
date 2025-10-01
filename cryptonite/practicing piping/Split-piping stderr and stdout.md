# Split-piping stderr and stdout
This challenge asks us to redirect the standard ouput of /challenge/hack to one program and its standard error to another program to obtain the flag.
We will need to combine our knowledge of >(), 2>, and |.
# My solve
**Flag**-pwn.college{UQO7etKEU_7TF9tJMDggMzPxZ0m.QXxQDM2wyN5EzNzEzW}

>hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >(/challenge/the) > >(/challenge/planet)

>Congratulations, you have learned a redirection technique that even experts

>struggle with! Here is your flag:

>pwn.college{UQO7etKEU_7TF9tJMDggMzPxZ0m.QXxQDM2wyN5EzNzEzW}

# Reference
None.
