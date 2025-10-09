# Switching windows
This challenge asks us to switch windows (tmux) and get the flag.
# My solve
**Flag**-pwn.college{AfDSJ2xv2oXv-PjkRqS9Mp595VS.0FM5IDOxwyN5EzNzEzW}

Main Terminal:

>hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux a

Window 1

> cat <<MSG

>Welcome to the tmux window switching challenge!

>You are currently in window 1.

>The flag is hidden in window 0.

>Use Ctrl-B 0 to switch to window 0!

>MSG

>hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG

> > Welcome to the tmux window switching challenge!

> > You are currently in window 1.

> > The flag is hidden in window 0.

> > Use Ctrl-B 0 to switch to window 0!

> > MSG

>Welcome to the tmux window switching challenge!

>You are currently in window 1.

>The flag is hidden in window 0.

>Use Ctrl-B 0 to switch to window 0!

ctrl B 0

Window 0

>hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG

> > Excellent work! You found window 0!

> > Here is your flag: pwn.college{AfDSJ2xv2oXv-PjkRqS9Mp595VS.0FM5IDOxwyN5EzNzEzW}

> > MSG

>Excellent work! You found window 0!

>Here is your flag: pwn.college{AfDSJ2xv2oXv-PjkRqS9Mp595VS.0FM5IDOxwyN5EzNzEzW}

# What I learned
Just like screen, tmux has windows. The key combos are different, but the concept is the same:

Ctrl-B c - Create a new window

Ctrl-B n - Next window

Ctrl-B p - Previous window

Ctrl-B 0 through Ctrl-B 9 - Jump to window 0-9

Ctrl-B w - See a nice window picker

# Reference
None
