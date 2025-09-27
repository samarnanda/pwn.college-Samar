# grepping for a needle in a haystack
This challenge asks us to find the flag from within a file containing a hundred thousand lines, by using the grep command.
# My solve
**Flag**- pwn.college{0Rd9ze3biXcGnArJUK998b6DpCJ.QX3EDO0wyN5EzNzEzW}

We invoke the "grep" command for this task. Sometimes, the files that we read using car can be too big. So we use the grep command to search for the specific content we want to read from the file instead of the entire file.
The grep command takes the search string and the path to the file as arguments respectively.
So, the full command for this task is: grep pwn.college /challenge/data.txt. The path to file is /data.txt and the flag always starts from "pwn.college".

>hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt

>pwn.college{0Rd9ze3biXcGnArJUK998b6DpCJ.QX3EDO0wyN5EzNzEzW}

# What I learned
I learned that grep will search the file for lines of text containing the search string ("pwn.college" in our case) and print them to the console.
There are many ways to grep. "grep search_string /path/to/file" is one of these ways.
# References
None.
