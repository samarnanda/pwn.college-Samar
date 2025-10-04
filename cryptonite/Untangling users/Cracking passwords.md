# Cracking passwords
This new challenge asks us to crack the password of zardus using "John the ripper" and then su to zardus and run the command which will get us the flag.
# My solve
**Flag**-pwn.college{gbkYA8LuYwniwnd8mQg9cX7IrY_.QX3UDN1wyN5EzNzEzW}

>hacker@users~cracking-passwords:~$ john /challenge/shadow-leak

>Loaded 1 password hash (crypt, generic crypt(3) [?/64])

>Press 'q' or Ctrl-C to abort, almost any other key for status

>0g 0:00:00:18 1% 2/3 0g/s 290.6p/s 290.6c/s 290.6C/s chacha..jazmin

>aardvark         (zardus)

>1g 0:00:00:20 100% 2/3 0.04995g/s 290.8p/s 290.8c/s 290.8C/s Johnson..buzz

>Use the "--show" option to display all of the cracked passwords reliably

>Session completed

>hacker@users~cracking-passwords:~$ su zardus

>Password:

>zardus@users~cracking-passwords:/home/hacker$ /challenge/run

>Congratulations, you have become Zardus! Here is your flag:

>pwn.college{gbkYA8LuYwniwnd8mQg9cX7IrY_.QX3UDN1wyN5EzNzEzW}

# What I learned
If we have the hashed value of the password, we can crack it.
When we input a password into su, it one-way-encrypts (hashes) it and compares the result against the stored value. If the result matches, su grants you access to the user.
John the ripper cracks the leaked password hash to find the real value.
# Reference
None
