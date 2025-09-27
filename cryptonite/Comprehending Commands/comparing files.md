# comparing files
This challenge asks us to compare two files using the "diff" command and find the flag. The first file contains 100 fake flags and the second file contains all the fake flags along with the real one.
First file is "decoys_only.txt" and second is "decoys_and_real.txt". Both are in the challenge directory.
# My solve

We invoke the "diff" command and put the two files as arguments in the command line. 
The full command is: diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
This gives us the flag as the only thing different between the two files is the real flag.

>hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt

>69a70

>> pwn.college{IpU1Ci5yJZTKCm_8xeJmHnMFK6G.01MwMDOxwyN5EzNzEzW}
# What I learned
I learned that diff compares two files line by line and shows you exactly what's different between them. It also tells that which line is replaced by what amongst the two files.
It also tells us if a file has an additional line and where that line is. "69a70" means that "after line 69 of file decoys_only.txt, add line 70 of file decoys_and_real.txt".
# Reference
None.
