# Resuming processes
This challenge asks us to run and suspend a process then resume it using the "fg" command to obtain the flag.
# My solve
**Flag**-pwn.college{0-T2lbIhZ2w4PFCfH4mh2fQ025Q.QX2QDO0wyN5EzNzEzW}

>hacker@processes~resuming-processes:~$ /challenge/run

>Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with

>the 'fg' command! Or just press Enter to quit me!

>^Z

>[1]+  Stopped                 /challenge/run

>hacker@processes~resuming-processes:~$ fg

>/challenge/run

>I'm back! Here's your flag:

>pwn.college{0-T2lbIhZ2w4PFCfH4mh2fQ025Q.QX2QDO0wyN5EzNzEzW}

>Don't forget to press Enter to quit me!

>Goodbye!

# What I learned
To resume processes, your shell provides the fg command, a builtin that takes the suspended process, resumes it, and puts it back in the foreground of your terminal.
# Reference
None
