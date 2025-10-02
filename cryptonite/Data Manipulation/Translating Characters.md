# Translating Characters
This challenge asks us to run the program which prints the flag but swaps the casing of all characters. We need to undo this by using "tr" to obtain the actual flag.
# My solve
**Flag**- pwn.college{EH1m9EQqtuSvVnRUXXRUFqaZvk_.01MxEzNxwyN5EzNzEzW}

>hacker@data~translating-characters:~$ /challenge/run | tr 'a-zA-Z' 'A-Za-z'

>yOUR CASE-SWAPPED FLAG:

>pwn.college{EH1m9EQqtuSvVnRUXXRUFqaZvk_.01MxEzNxwyN5EzNzEzW}

# What I learned
I learned that "tr" translates characters it receives over standard input and prints them to standard output.
In its most basic usage, tr translates the character provided in its first argument to the character provided in its second argument.

# Reference
None.
