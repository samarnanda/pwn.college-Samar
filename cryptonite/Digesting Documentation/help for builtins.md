# Help for builtins
This challenge asks us to use the "help" builtin with the "challenge" shell builtin to look up the help of the "challenge" and obtain the secret value which we need to pass as the argument in order to get the flag.
# My solve
**Flag**-pwn.college{wzFDH__xQ4i6imVPkEGYjxgFtbv.QX0ETO0wyN5EzNzEzW}

>hacker@man~help-for-builtins:~$ help challenge

>challenge: challenge [--fortune] [--version] [--secret SECRET]

>    This builtin command will read you the flag, given the right arguments!

>    Options:

>      --fortune         display a fortune

>      --version         display the version
 
 >     --secret VALUE    prints the flag, if VALUE is correct

>    You must be sure to provide the right value to --secret. That value

>    is "wzFDH__x".

>hacker@man~help-for-builtins:~$ challenge --secret wzFDH__x

>Correct! Here is your flag!

>pwn.college{wzFDH__xQ4i6imVPkEGYjxgFtbv.QX0ETO0wyN5EzNzEzW}

# References
None.
