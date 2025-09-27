# home sweet home
This challenge asks us to copy the flag into another file from "/chellenge/run". It will write a copy of the flag to any file we specify as an argument on the command line as long as it meets these conditions:
1) Your argument must be an absolute path.
2) The path must be inside your home directory.
3) Before expansion, your argument must be three characters or less.
# My solve 
**Flag**-pwn.college{EmfSYfxJ4pKHapBI4sE4i4reClb.QXzMDO0wyN5EzNzEzW}

We need to invoke the /challenge/run command first and then provide a path to the file we want the flag to be copied at according to the conditions.
We use "~" to represent "/home/hacker/" as it is the current working directory, to obey the 3rd condition. Let the name of our file be "f", so our absolute path to the file "f" would be "/home/hacker/f".
so our full command will be: /challenge/run ~/f. This copies the flag into the f file which is in the /home/hacker directory.
>hacker@paths~home-sweet-home:~$ /challenge/run ~/f

>Writing the file to /home/hacker/f!

>... and reading it back to you:

>pwn.college{EmfSYfxJ4pKHapBI4sE4i4reClb.QXzMDO0wyN5EzNzEzW}
# What I Learned
I learned that "~" represents the home directory (specifically /home/hacker/ as the user is hacker). 
Whenever bash sees ~ provided as the start of an argument in a way consistent with a path, it will expand it to your home directory. 
I also learned that only the leading "~" is expanded, for example, that ~/~ will be expanded to /home/hacker/~ rather than /home/hacker/home/hacker.
# References
None.
