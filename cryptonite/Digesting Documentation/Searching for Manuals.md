# Searching for Manuals
This challenge asks us to find the flag from obtaining information from the manual, by using the appropriate argument, which we will know from the manual.
The name of the manual is randomized in this one, but we can get to know the name from the database by using the man man command and reading the manual to get the actual name of the manual in which the flag is in.
# My solve

hacker@man~searching-for-manuals:~$ man man

hacker@man~searching-for-manuals:~$ man man.1

hacker@man~searching-for-manuals:~$ man -k flag

dpkg-buildflags (1)  - returns build flags to use during package build

Dpkg::BuildFlags (3perl) - query build flags

errwmawiuw (1)       - print the flag!

fegetexceptflag (3)  - floating-point rounding and exception handling

fesetexceptflag (3)  - floating-point rounding and exception handling

i386 (8)             - change reported architecture in new program environment and/or set personality flags

ioctl_iflags (2)     - ioctl() operations for inode flags

linux32 (1)          - change reported architecture in new program environment and/or set personality flags

linux64 (1)          - change reported architecture in new program environment and/or set personality flags

pcap-config (1)      - write libpcap compiler and linker flags to standard output

security_compute_av_flags (3) - query the SELinux policy database in the kernel

security_compute_av_flags_raw (3) - query the SELinux policy database in the kernel

set_matchpathcon_flags (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of validity checking and error displaying

set_matchpathcon_invalidcon (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of validity checking and error displaying

set_matchpathcon_printf (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of validity checking and error displaying

setarch (1)          - change reported architecture in new program environment and/or set personality flags

setarch (8)          - change reported architecture in new program environment and/or set personality flags

x86_64 (8)           - change reported architecture in new program environment and/or set personality flags

hacker@man~searching-for-manuals:~$ man errwmawiuw

hacker@man~searching-for-manuals:~$ /challenge/challenge --errwma 669

Correct usage! Your flag: pwn.college{YerCZ6WWSrwFma6Nw9iUTV-5YNu.QX2EDO0wyN5EzN

# Reference
None.
