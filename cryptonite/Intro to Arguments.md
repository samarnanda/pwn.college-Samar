# Intro to Arguments
This challenge asks you to open the terminal in pwn.college dojo and invoke commands such as "echo" and "hello" while using multiple arguments for obtaining different results.
# My Solve
**Flag**:pwn.college{UgWFU7X0kH-lGtCEOBUSiSLaOht.QX4YjM1wyN5EzNzEzW}
First, we execute the "echo" command with the "Hello" argument, the terminal displays "Hello". we then execute "echo" command with two arguments (as it can take mnultiple arguments) "Hello" and "Hackers". The terminal then displays "Hello Hackers". We then execute the "hello" command with "hackers" argument to obtain the flag.
>hacker@hello~intro-to-arguments:~$ echo Hello
>Hello
>hacker@hello~intro-to-arguments:~$ echo Hello Hackers!
>Hello Hackers!
>hacker@hello~intro-to-arguments:~$ hello hackers
>Success! Here is your flag:
>pwn.college{UgWFU7X0kH-lGtCEOBUSiSLaOht.QX4YjM1wyN5EzNzEzW}
# What I Learned
I learned that Linux commands can take multpiple arguments and that they are also case sensitive. The first word is the command and the subsequent words are the arguments. I also learned the function of the "echo" command which displays the argument as an ouput.
# References
None.
