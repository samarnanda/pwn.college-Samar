# Handling failure
This challenge asks us to chain two commands using "||" and run them to get the flag.
# My solve
**Flag**-pwn.college{kw-_k38eAiOW16IVX7Rp8jnqtQH.01M0MDOxwyN5EzNzEzW}

>hacker@chaining~handling-failure:~$ /challenge/first-failure ||  /challenge/second

>Nice chaining! Flag: pwn.college{kw-_k38eAiOW16IVX7Rp8jnqtQH.01M0MDOxwyN5EzNzEzW}

# What I learned
The || operator allows you to run a second command only if the first command fails (exits with a non-zero code). This is called the "OR" operator because either the first command succeeds OR the second command will run.

# Reference
None.
