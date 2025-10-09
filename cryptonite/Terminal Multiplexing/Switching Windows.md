# Switching Windows
This challenge asks us to reattach to window 1, which then shows us a welcome message. We then switch to window 0 using the command "ctrl A 0" and then get the flag.
# My solve
**Flag**-pwn.college{oHrQWwUXbbkt_Fr0E0tHeTKNq6n.0FO4IDOxwyN5EzNzEzW}

Main Terminal:

>hacker@terminal-multiplexing~switching-windows:~$ screen -r

>[detached from 135.challenge_session]

Window 1:

> cat <<MSG

>Welcome to the window switching challenge!

>You are currently in window 1.

>The flag is hidden in window 0.

>Use Ctrl-A 0 to switch to window 0!

>MSG

>hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG

> > Welcome to the window switching challenge!

> > You are currently in window 1.

> > The flag is hidden in window 0.

> > Use Ctrl-A 0 to switch to window 0!

> > MSG

>Welcome to the window switching challenge!

>You are currently in window 1.

>The flag is hidden in window 0.

>Use Ctrl-A 0 to switch to window 0!

ctrl A 0

Window 0:

>hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG

> > Excellent work! You found window 0!

> > Here is your flag: pwn.college{oHrQWwUXbbkt_Fr0E0tHeTKNq6n.0FO4IDOxwyN5EzNzEzW}

> > MSG

>Excellent work! You found window 0!

>Here is your flag: pwn.college{oHrQWwUXbbkt_Fr0E0tHeTKNq6n.0FO4IDOxwyN5EzNzEzW}

# What I learned
Windows are handled with different keyboard shortcuts, all starting with Ctrl-A:

Ctrl-A c - Create a new window

Ctrl-A n - Next window

Ctrl-A p - Previous window

Ctrl-A 0 through Ctrl-A 9 - Jump directly to window 0-9

Ctrl-A " - bring up a selection menu of all of the windows

# Reference
None.
