# Multiple options for tab completion
This challenge asks us to keep using the tab key to look for the file in which the flag is, step by step.
# My solve

>hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-

>pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  pwncollege-hacking

>hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-f

>pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter

>hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-fl

>pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter

>hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-fla

>pwncollege-flag      pwncollege-flamingo

>hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-flag

>hack-the-planet        pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking

>pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter

>hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-flag

>pwn.college{cxkJtE9cDcXaU_ja9cwL7ZkjGA6.0lN0EzNxwyN5EzNzEzW}

# What I learned 
I learned that, when there are multiple options, by default bash will auto-expand until the first point when there are multiple options (in this case, fl). When you hit tab a second time, it'll print out those options. Other shells and configurations, instead, will cycle through the options.
# Reference
None.
