# Tab completion 
This challenge asks us to read the file using "tab" in the shell instead of typing out the name of the file and then obtain the flag.
# My solve
**Flag**-pwn.college{Y5NcAwIsz31q2LaAZIWnCYlg-WA.QX2IDO0wyN5EzNzEzW}

>hacker@globbing~tab-completion:~$ ls /challenge

>DESCRIPTION.md  pwncollege​

>hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​

>pwn.college{s3B6EAvoMCo2LCIpr8gp0BXBaqA.0FN0EzNxwyN5EzNzEzW}

# What I learned
I learned that using * can cause errors and a much better way is to use the "tab" key in the shell which will predict what we are going to type and auto complete it.
# Reference
None.
