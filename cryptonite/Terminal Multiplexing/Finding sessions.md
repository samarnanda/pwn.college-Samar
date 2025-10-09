# Finding sessions
This challenge asks us to check different screens to look for the flag. There are some decoy screens which dont contain the flag, only one contains the flag.
We check different screens by giving pid or name as argument for "screen -r".
# My solve
**Flag**-pwn.college{UXWzPvt2ribC31jRyMjDurSx7RQ.01N4IDOxwyN5EzNzEzW}

Main Terminal:

>hacker@terminal-multiplexing~finding-sessions:~$ screen -ls

>There are screens on:

>    173.pts-1.terminal-multiplexing~launching-screen        (Remote or dead)

>    144.session_0f5f9c76deca41fa    (Detached)

>    147.session_f7ad35bbbb6eaf70    (Detached)

>    150.session_3f72265af010afee    (Detached)

>4 Sockets in /home/hacker/.screen.

>hacker@terminal-multiplexing~finding-sessions:~$ screen -r 173

>There is a screen on:

>    173.pts-1.terminal-multiplexing~launching-screen        (Dead ???)

>Remove dead screens with 'screen -wipe'.

>There is no screen to be resumed matching 173.

>hacker@terminal-multiplexing~finding-sessions:~$ screen -wipe

>There are screens on:

>    173.pts-1.terminal-multiplexing~launching-screen        (Remote or dead)

>    144.session_0f5f9c76deca41fa    (Detached)

>    147.session_f7ad35bbbb6eaf70    (Detached)

>    150.session_3f72265af010afee    (Detached)

>4 Sockets in /home/hacker/.screen.

>hacker@terminal-multiplexing~finding-sessions:~$ screen -r 144

>[detached from 144.session_0f5f9c76deca41fa]

Screen 1:

>hacker@terminal-multiplexing~finding-sessions:~$  echo 'Nothing here! Try another session.'

>Nothing here! Try another session.

Main Terminal:

>hacker@terminal-multiplexing~finding-sessions:~$ screen -r 147

>[detached from 147.session_f7ad35bbbb6eaf70]

Screen 2:

>hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'

>Congratulations! You found the right session!

>hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{UXWzPvt2ribC31jRyMjDurSx7RQ.01N4IDOxwyN5EzNzEzW}

>pwn.college{UXWzPvt2ribC31jRyMjDurSx7RQ.01N4IDOxwyN5EzNzEzW}

# What I learned
The identifiers of the sessions are the PID of each respective screen process, a dot, and the name of the screen session. To attach to a specific one, we use its name or its PID by giving it as an argument to screen -r.
# Reference
None.
