# An epic filesystem quest
This challenge asks us to go on an epic file system quest
# My solve 
**Flag**- pwn.college{06sITtLmCprGFKCQ-JFd0Wu_Ewk.QX5IDO0wyN5EzNzEzW}

hacker@commands~an-epic-filesystem-quest:/$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls -a
.  ..  .dockerenv  ALERT  bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~an-epic-filesystem-quest:/$ cat ALERT
Tubular find!
The next clue is in: /usr/local/lib/python3.8/dist-packages/sympy/polys/numberfields/tests

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ ls /usr/local/lib/python3.8/dist-packages/sympy/polys/numberfields/tests
SNIPPET-TRAPPED  __init__.py  __pycache__  test_basis.py  test_galoisgroups.py  test_minpoly.py  test_modules.py  test_numbers.py  test_primes.py  test_subfield.py  test_utilities.py
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/local/lib/python3.8/dist-packages/sympy/polys/numberfields/tests/SNIPPET-TRAPPED
Yahaha, you found me!
The next clue is in: /usr/share/doc/python3-chardet

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ cd  /usr/share/doc/python3-chardet
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/python3-chardet$ ls -a
.  ..  .INFO  changelog.Debian.gz  copyright
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/python3-chardet$ cat .INFO
Tubular find!
The next clue is in: /usr/local/lib/python3.8/dist-packages/sympy/strategies/branch/tests

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/python3-chardet$ cd /usr/local/lib/python3.8/dist-packages/sympy/strategies/branch/tests
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/strategies/branch/tests$ ls -a
.  ..  .HINT  __init__.py  __pycache__  test_core.py  test_tools.py  test_traverse.py
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/strategies/branch/tests$ cat .HINT
Tubular find!
The next clue is in: /usr/share/doc/git/contrib/credential

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/strategies/branch/tests$ cd  /usr/share/doc/git/contrib/credential
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/git/contrib/credential$ ls -a
.  ..  .EVIDENCE  gnome-keyring  libsecret  netrc  osxkeychain  wincred
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/git/contrib/credential$ cat .EVIDENCE
Congratulations, you found the clue!
The next clue is in: /usr/lib/python3/dist-packages/hyperlink/test

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/git/contrib/credential$ ls /usr/lib/python3/dist-packages/hyperlink/test
NUGGET-TRAPPED  __init__.py  __pycache__  common.py  test_common.py  test_decoded_url.py  test_parse.py  test_scheme_registration.py  test_url.py
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/git/contrib/credential$ cat /usr/lib/python3/dist-packages/hyperlink/test/NUGGET-TRAPPED
Tubular find!
The next clue is in: /opt/linux/linux-5.4/Documentation/networking/device_drivers/toshiba

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/git/contrib/credential$ cd /opt/linux/linux-5.4/Documentation/networking/device_drivers/toshiba
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/networking/device_drivers/toshiba$ ls
CLUE  spider_net.txt
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/networking/device_drivers/toshiba$ cat CLUE
Lucky listing!
The next clue is in: /usr/share/icons/Adwaita/scalable

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/networking/device_drivers/toshiba$ cd /usr/share/icons/Adwaita/scalable
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Adwaita/scalable$ ls -a
.  ..  .MESSAGE  actions  apps  categories  devices  emblems  emotes  legacy  mimetypes  places  status  ui
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Adwaita/scalable$ cat .MESSAGE
Yahaha, you found me!
The next clue is in: /opt/busybox/busybox-1.33.2/include/config/feature/verbose/cp
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/Adwaita/scalable$ cd /opt/busybox/busybox-1.33.2/include/config/feature/verbose/cp
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/verbose/cp$ ls
INSIGHT  message.h
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/verbose/cp$ cat INSIGHT
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{06sITtLmCprGFKCQ-JFd0Wu_Ewk.QX5IDO0wyN5EzNzEzW}
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/verbose/cp$

# References 
None.
