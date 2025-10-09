# Detaching and attaching
This challenge asks us to launch screen and detach from it, then run a program which will print the flag to our detached session.
We then reattach to our screen and get the flag.
# My solve
**Flag**-pwn.college{8eRTpIDNUpIYA3_oonsVKWS6Krq.0lN4IDOxwyN5EzNzEzW}

screen:

>hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{8eRTpIDNUpIYA3_oonsVKWS6Krq.0lN4IDOxwyN5EzNzEzW}

>Yes! Flag is: pwn.college{8eRTpIDNUpIYA3_oonsVKWS6Krq.0lN4IDOxwyN5EzNzEzW}

main command line:

>hacker@terminal-multiplexing~launching-screen:~$ screen

>[detached from 162.pts-0.terminal-multiplexing~detaching-and-attaching]

>hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run

>Found detached screen session: 162.pts-0.terminal-multiplexing~detaching-and-attaching

>Sending flag to your screen session...


>Flag sent! Now reattach to your screen session with:

 
  >screen -r


>You'll find the flag waiting for you there!

>hacker@terminal-multiplexing~detaching-and-attaching:~$ screen -r

>[screen is terminating]

# What I learned
When we are working on the normal terminal and our connection drops, our progress can be lost. With screen, our work keeps running, and you can reattach later.
# Reference
None
