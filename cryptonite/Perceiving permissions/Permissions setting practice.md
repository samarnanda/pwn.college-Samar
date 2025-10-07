# Permissions setting practice
This challenge asks us to go on a 8-round game in which we have to set permissions using "chmod" according to the round rules and after completing 8 rounds we have to make the flag readable and read it.
# My solve
**Flag**-pwn.college{IUQED914X4OPUm8othr-TW5t19u.QXzETO0wyN5EzNzEzW}

hacker@permissions~permissions-setting-practice:~$ /challenge/run

Round 1 of 8!

Current permissions of "/challenge/pwn": rw-r--r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": ----w-r--
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

hacker@permissions~permissions-setting-practice:~$ chmod u=-,g=w,o=r /challenge/pwn

You set the correct permissions!

Round 2 of 8!

Current permissions of "/challenge/pwn": ----w-r--
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": r-xr-----
* the user does have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

hacker@permissions~permissions-setting-practice:~$ chmod u=rx,g=r,o=- /challenge/pwn

You set the correct permissions!

Round 3 of 8!

Current permissions of "/challenge/pwn": r-xr-----
* the user does have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rwxrw---x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

hacker@permissions~permissions-setting-practice:~$ chmod u=rwx,g=rw,o=x /challenge/pwn

You set the correct permissions!

Round 4 of 8!

Current permissions of "/challenge/pwn": rwxrw---x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": --x-w-rwx
- the user doesn't have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

hacker@permissions~permissions-setting-practice:~$ chmod u=x,g=w,o=xrw /challenge/pwn

You set the correct permissions!

Round 5 of 8!

Current permissions of "/challenge/pwn": --x-w-rwx
- the user doesn't have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": ----wxr-x
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

hacker@permissions~permissions-setting-practice:~$ chmod u=-,g=wx,o=rx /challenge/pwn

You set the correct permissions!

Round 6 of 8!

Current permissions of "/challenge/pwn": ----wxr-x
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": --x--xr--
- the user doesn't have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

hacker@permissions~permissions-setting-practice:~$ chmod u=x,g=x,o=r /challenge/pwn

You set the correct permissions!

Round 7 of 8!

Current permissions of "/challenge/pwn": --x--xr--
- the user doesn't have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": r--r-x-wx
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
* the world does have execute permissions

hacker@permissions~permissions-setting-practice:~$ chmod u=r,g=rx,o=wx /challenge/pwn

You set the correct permissions!

Round 8 of 8!

Current permissions of "/challenge/pwn": r--r-x-wx
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": rw----rwx
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

hacker@permissions~permissions-setting-practice:~$ chmod u=rw,g=-,o=rwx /challenge/pwn

You set the correct permissions!

You've solved all 8 rounds! I have changed the ownership
of the /flag file so that you can 'chmod' it. You won't be able to read
it until you make it readable with chmod!

Current permissions of "/flag": ---------
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

hacker@permissions~permissions-setting-practice:~$ chmod a+r /flag

hacker@permissions~permissions-setting-practice:~$ cat /flag

pwn.college{IUQED914X4OPUm8othr-TW5t19u.QXzETO0wyN5EzNzEzW}

# Reference 
None
