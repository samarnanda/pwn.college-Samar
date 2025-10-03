# Backgrounding processes
This challenge asks us to launch a process then suspend it, then background it using "bg" and launch another copy while the first is running in the background.
# My solve
**Flag**-pwn.college{g9525Uh9qLPgJSk9KEl49vnZlif.QX3QDO0wyN5EzNzEzW}

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         160 S+   bash /challenge/run
root         162 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the
background, and then launch a new version of me! You can background me with
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         160 S    bash /challenge/run
root         170 S    sleep 6h
root         171 S+   bash /challenge/run
root         173 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{g9525Uh9qLPgJSk9KEl49vnZlif.QX3QDO0wyN5EzNzEzW}

# What I learned
You can also resume processes in the background with the bg command! This will allow the process to keep running, while giving you your shell back to invoke more commands in the meantime.
# Reference
None.
