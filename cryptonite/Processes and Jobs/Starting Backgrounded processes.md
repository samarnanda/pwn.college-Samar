# Starting backgrounded processes
This challenge asks us to background a process without suspending it by appending a "&" to the command.
# My solve
**Flag**-pwn.college{ELC24eG5moqKllO2ZmMEImTis-M.QX5QDO0wyN5EzNzEzW}

hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 161
hacker@processes~starting-backgrounded-processes:~$


Yay, you started me in the background! Because of that, this text will probably
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{ELC24eG5moqKllO2ZmMEImTis-M.QX5QDO0wyN5EzNzEzW}

# What I learned
We don't have to suspend processes to background them: we can start them backgrounded right off the bat! It's easy; all we have to do is append a & to the command.
# Reference
None
