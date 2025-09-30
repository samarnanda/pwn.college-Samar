# Filtering with grep -v
This challenge asks us to obtain the flag by grep -v method which prints all the lines that DO NOT contain the phrase we put as the argument.
# My solve
**Flag**- pwn.college{gAaL3Ds0it3PnWCWBfTOyOlSmf0.0FOxEzNxwyN5EzNzEzW}

>hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY

>pwn.college{gAaL3Ds0it3PnWCWBfTOyOlSmf0.0FOxEzNxwyN5EzNzEzW}

# What I learned
The grep command has a very useful option: -v (invert match). While normal grep shows lines that MATCH a pattern, grep -v shows lines that do NOT match a pattern.

# reference
None
