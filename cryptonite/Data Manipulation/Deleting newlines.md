# Deleting newlines
This challenge asks us to delete the newline characer "\n" fromt the flag in order to get the actual flag, by using -d as argument for tr.
# My solve
**Flag**-pwn.college{MpUIDVo9KFAIscM3jA61ZFyOosg.0VNxEzNxwyN5EzNzEzW}

>hacker@data~deleting-newlines:~$ /challenge/run | tr -d '\n'

>Your line-split flag: pwn.college{MpUIDVo9KFAIscM3jA61ZFyOosg.0VNxEzNxwyN5EzNzEzW}

# What I learned
Here, the backslash (\) signifies that the character that follows it is a standin for a character that's hard to input into the shell normally. The newline, of course, is hard to input because when you typically hit Enter, you'll run the command itself. \n is a standin for this newline, and it must be in quotes to prevent the shell interpreter itself from trying to interpret it and pass it to tr instead.
# Reference
None.
