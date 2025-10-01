# Named Pipes
This challenge asks us to create a /tmp/flag_fifo file and redirect the stdout of /challenge/run to it to obtain the flag.
# My solve
**Flag**-pwn.college{8_UpS-Yh8W4MELMd7ttU67IksNM.01MzMDOxwyN5EzNzEzW}

First time we open the terminal:
>hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo

>hacker@piping~named-pipes:~$ cat /tmp/flag_fifo

We then close the terminal and open it again:
>hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo

>You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo!

>Bash will now try to open the FIFO for writing, to pass it as the stdout of

>/challenge/run. Recall that operations on FIFOs will *block* until both the

>read side and the write side is open, so /challenge/run will not actually be

>launched until you start reading from the FIFO!

>hacker@piping~named-pipes:~$ cat /tmp/flag_fifo

>You've correctly redirected /challenge/run's stdout to a FIFO at

>/tmp/flag_fifo! Here is your flag:

>pwn.college{8_UpS-Yh8W4MELMd7ttU67IksNM.01MzMDOxwyN5EzNzEzW}

# What I learned
You can also create your own persistent named pipes that stick around on the filesystem! These are called FIFOs, which stands for First (byte) In, First (byte) Out.
Unlike the automatic named pipes from process substitution:

You control where FIFOs are created
They persist until you delete them
Any process can write to them by path (e.g., echo hi > my_pipe)
You can see them with ls and examine them like files

One problem with FIFOs is that they'll "block" any operations on them until both the read side of the pipe and the write side of the pipe are ready.

Of course, this can somewhat be done by normal files: you've learned how to echo stuff into them and cat them out. Why use a FIFO instead? Here are key differences:

No disk storage: FIFOs pass data directly between processes in memory - nothing is saved to disk
Ephemeral data: Once data is read from a FIFO, it's gone (unlike files where data persists)
Automatic synchronization: Writers block until the readers are ready, and vice-versa. This is actually useful! It provides automatic synchronization. Consider the example above: with a FIFO, it doesn't matter if cat myfifo or echo pwn > myfifo is executed first; each would just wait for the other. With files, you need to make sure to execute the writer before the reader.
Complex data flows: FIFOs are useful for facilitating complex data flows, merging and splitting data in flexible ways, and so on. For example, FIFOs support multiple readers and writers.

# Reference
None.
