# Extracting specific sections of a text
This challenge asks us to run a program, extract the second column of that text and then delete the newline character so that we can get the flag.
# My solve
**Flag**-pwn.college{Up0DcykLR8QX6NWWCDh2RdeG1J8.01NxEzNxwyN5EzNzEzW}

>hacker@data~extracting-specific-sections-of-text:~$ /challenge/run

>19386 p

>20077 w

>4035 n

>30185 .

>16640 c

>9837 o

>25056 l

>23920 l

>32575 e

>14542 g

>2443 e

>11182 {

>21255 U

>666 p

>21525 0

>26747 D

>9025 c

>2838 y

>23473 k

>27820 L

>9549 R

>27648 8

>1552 Q

>11276 X

>26426 6

>6673 N

>32631 W

>6776 W

>19602 C

>5697 D

>5806 h

>4577 2

>28935 R

>8946 d

>25993 e

>3963 G

>3164 1

>29722 J

>4529 8

>5371 .

>10633 0

>7557 1

>3787 N

>26501 x

>29246 E

>20797 z

>1485 N

>24348 x

>21946 w

>19037 y

>13153 N

>12015 5

>25134 E

>25744 z

>17164 N

>31175 z

>11046 E

>27533 z

>9951 W

>6581 }

>hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"

>pwn.college{Up0DcykLR8QX6NWWCDh2RdeG1J8.01NxEzNxwyN5EzNzEzW}

# What I learned
The 'cut" command is used to extract specific columns of text. We also specify the column delimitter.
# Reference
None.
