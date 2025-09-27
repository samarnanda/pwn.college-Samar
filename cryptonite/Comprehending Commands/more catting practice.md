# more catting practice
this challenge asks us to read the file and obtain the flag by using cat command. Since the "flag" file is in a different directory and we are not allowed to use the "cd" command, we have to use the absolute path of the "flag" file as the argument.
# My solve
**Flag**- pwn.college{M0zy739FupS6dYTiCQzqm0jP0er.QXwITO0wyN5EzNzEzW}

We execute the cat command with the absolute path of the flag file as the argument. "flag" is in a different directory and we cannot use the cd command to change the directory.
The directory in which "flag" is: /usr/share/aclocal/flag. So our full command would be: cat /usr/share/aclocal/flag

>hacker@commands~more-catting-practice:~$ cat /usr/share/aclocal/flag

>pwn.college{M0zy739FupS6dYTiCQzqm0jP0er.QXwITO0wyN5EzNzEzW}

# What I learned
I learned that we provide the absolute path of a file as the argument in the cat command as well, apart from just the file name.
# Refernces
None.
