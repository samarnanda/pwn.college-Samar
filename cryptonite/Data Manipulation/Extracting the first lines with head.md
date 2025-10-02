# Extracting the first lines with head
This challenge asks us to pipe a program through "head" and get just the first 7 lines and then pipe these lines further onwords to another program to get the flag.
# My solve
**Flag**-pwn.college{Y90YUsBngAqUrqx-PwR7bXDk8wk.0lNxEzNxwyN5EzNzEzW}

>hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | tee >(/challenge/college)

>SECRET-CODE-13952

>SECRET-CODE-5106

>SECRET-CODE-32224

>SECRET-CODE-9204

>SECRET-CODE-1082

>SECRET-CODE-13199

>SECRET-CODE-1077

>Congratulations, you piped the right codes!

>hacker@data~extracting-the-first-lines-with-head:~$ pwn.college{Y90YUsBngAqUrqx-PwR7bXDk8wk.0lNxEzNxwyN5EzNzEzW}

# What I learned
The head command is used to display the first few lines of its input. By default, it shows the first 10 lines, but you can control this with the -n option.
We provide the number of lines we want as the argument for "-n".
# Reference
None.
