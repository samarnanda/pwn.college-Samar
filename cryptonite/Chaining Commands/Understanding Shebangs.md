# Understanding Shebangs
This challenge asks us to ceate a script with a proper shebang and appropriate output, make it executable and the run a program to obtain the flag.
# My solve
**Flag**-pwn.college{ksuA1_vFqzOtweKy2eBB0q16G9n.0VOzMDOxwyN5EzNzEzW}

>hacker@chaining~understanding-shebangs:~$ chmod a+x /home/hacker/solve.sh

>hacker@chaining~understanding-shebangs:~$ echo '#!/bin/bash' > /home/hacker/solve.sh

>hacker@chaining~understanding-shebangs:~$ echo 'echo "hack the planet"' >> /home/hacker/solve.sh

>hacker@chaining~understanding-shebangs:~$ /challenge/run

>Testing your script...

>Perfect! Your flag:

>Flag: pwn.college{ksuA1_vFqzOtweKy2eBB0q16G9n.0VOzMDOxwyN5EzNzEzW}
# What I learned
When a program is invoked in Linux, the Linux kernel first inspects the file to determine how it should be run. This does not use the extension.
Rather, Linux looks at the first few bytes of the file for this information.
# Reference
None
