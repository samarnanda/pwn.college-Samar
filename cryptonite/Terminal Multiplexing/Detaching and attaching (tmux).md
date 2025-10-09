# Detaching and attaching (tmux)
This challenge asks us to launch tmux, detach from it, then run a program which will send the flag to our detached session. We will then reattach to our session and get the flag.
# My solve
**Flag**-pwn.college{8fsDeEfbB2wr2jeT7gF9XrUuttS.0VO4IDOxwyN5EzNzEzW}

Main terminal:

>hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux

>[detached (from session 0)]

>hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run

>Found detached tmux session: 0

>Sending flag to your tmux session...


>Flag sent! Now reattach to your tmux session with:

>  tmux attach


>You'll find the flag waiting for you there!

>hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux a

>[detached (from session 0)]

tmux:

>hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{8fsDeEfbB2wr2jeT7gF9XrUuttS.0VO4IDOxwyN5EzNzEzW}

>Congratulations, here is your flag: pwn.college{8fsDeEfbB2wr2jeT7gF9XrUuttS.0VO4IDOxwyN5EzNzEzW}

# What I learned
tmux (terminal multiplexer) is screen's younger, more modern cousin. It does all the same things but with some different key bindings. 
The biggest difference is instead of Ctrl-A, tmux uses Ctrl-B as its command prefix.
# Reference
None.

