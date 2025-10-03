# Killing misbehaving processes
This process asks us to find the decoy program using "ps" and then kill the decoy program before running /challenge/run which will send the flag to a FIFO.
Once we read the fifo, it will print a lot of decoy flags, then we interrupt it and again run /challenge/run and read the fifo. This time it only prints the real flag.
# My solve
**Flag**-pwn.college{ct85ze07RMMs5DCSBYyeO3dXWN2.0FNzMDOxwyN5EzNzEzW}

hacker@processes~killing-misbehaving-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 10:35 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 10:35 ?        00:00:00 /run/dojo/bin/sleep 6h
root         137       1  0 10:35 ?        00:00:00 /bin/bash /challenge/.init
root         138       1  0 10:35 ?        00:00:00 /bin/bash /challenge/.init
root         139       1  0 10:35 ?        00:00:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
root         140     138  0 10:35 ?        00:00:00 sleep 6h
root         141     137  0 10:35 ?        00:00:00 sleep 6h
hacker       142     139  0 10:35 ?        00:00:00 /usr/bin/python /challenge/decoy
hacker       153       1  0 10:35 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --interface 0.0.0.0 --writable -t disableLeaveAlert true /run/dojo/bin/bash --login
hacker       186       0  0 10:36 pts/1    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoint
hacker       192     186  0 10:36 pts/1    00:00:00 /run/dojo/bin/bash --login
hacker       201     153  0 10:38 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       211       0  0 10:40 pts/2    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoint
hacker       217     211  0 10:40 pts/2    00:00:00 /run/dojo/bin/bash --login
hacker       226     217  0 10:40 pts/2    00:00:00 ps -ef
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
^C
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{P7bQ2b-.5Z3svdmb0kdXETuL5jpqNKDErmx5mu.T.nrBqiR}
pwn.college{GbC8fLpbthEMEkdBpey9BduqNVBKKwEvXQEJ4UCxYhiOj4b}
pwn.college{ey2Tw3dlPwUzVcwlmzjb0dVNhqwgkHXPTuag5cUqIyPRFG5}
pwn.college{G7LpFkoRdIrCU5W0pCRzYDbNLIiqxDr7Zc8L4TML708IH0R}
pwn.college{BaztI4mWSSFYu5YCousE6UwEiWs7oi9tQJfSCf49F5ssbNK}
pwn.college{bTtLIJZjadT2yG4FVJEXII6owSE7hVUuXrpbuHyOm9SFkGw}
pwn.college{lJZNw4HZl6HqYclFgdH634W.wsFEyM6tc49NUFhW9VTNs7J}
pwn.college{l0ltEoVj2tDv6SCIYdjvsHeHaSK.Ifk8bA20hd56l8n4JFB}
pwn.college{GmGxvs9ELEfO-yu.Hv1U.zbOH76ieWDTFzMzOko4jlz0SQK}
pwn.college{NsllOPJOMTwhxeJd5AfKMLJTp5E9pzQ84oeRRCR0co4fBoZ}
pwn.college{LYWIs9yyHE-lMn7.JCi5cLFMbCrQUuzDnTLmRr2n6ieHu8o}
pwn.college{-w7t1zW4LI0jPOZ6H6fGUnJgmyjs.9PYD2i5yfwtDVz1Nm4}
pwn.college{UHrgOkIc5QVJV4OnAiNygcWVTjArCEut9FvmNauL5RUylwC}
pwn.college{xrYzpYA-smvTwD49IWstPINx-g4FrnyfvclRjRwd-2NWTfn}
pwn.college{8uXMdlmShF3cDQZq.oswHWpy4A5F4GvPlch1mYVFnXw4tJv}
pwn.college{-T-7tDWrgrrLQS5Cb4n-WDPLA5SXRjPV0lo-odfpOJVO9w5}
pwn.college{wvA-YvgpIVlZPx-CYd0wBs918vmRqp800QFuoJEMefstpX5}
pwn.college{DG6DuvGRpRe24MpnkOy1H4ge-g3tfMe-98qE.nX6Ebw6w1r}
pwn.college{Oc6wdMhPAHe8U9Dm8JrEYK.sLUws6f-bjFAKe7QXZCHNqhj}
pwn.college{cxU4pI5.JS1EwNELbdKcU1Ve9OZA6UkHPhZJHOsd3.mXkLm}
pwn.college{KbnGPjKUyiMLzX3C0MzCPh7xDNKBEOL5z02HNyfx6YuqHV5}
pwn.college{b-ktoFYpwMffWEh5Fvkg-rRSHYaAk5zjdh84TL87O0KYiFP}
pwn.college{Ut3FUX04w103MQMX2gC7LrnQX1HDQrv9X09qg4tHyD8X9mF}
pwn.college{KgF5u5tPGc9ZcD-5bIWGOxQY9yyZncy1Jm1Q5EkniufwYyP}
pwn.college{vcFHzTZOi9yGnFBpQ.upvDIvJXPQQtYX.996w-dUpb71I.6}
pwn.college{p.d.zXjY9tWhoxxElYcZpxm.-p2PbdttGcdim-0w0pc4ZC6}
pwn.college{ycLN3hDhU1VWcm8.fOpnDbUJA7XMdvuZWaJn.zo9l9pCRJK}
pwn.college{RgrifaXys.1wgJalSwg.w8xMNtzJtRFfcDXPhauFgt.EDwI}
pwn.college{0sarp0HdeOu12o0vM44s6jR5iwKbLjZZ2DoXxYh8vso5gNM}
pwn.college{lA7fzFbUljAfLFEqaMDxnmTyIJAbVbPAPHxiI.XqSqU4waj}
pwn.college{UHdOcBM47XPDG.C6klrcLgkq4WKgkRVScQBTajeVSaBgB1F}
pwn.college{Kr.npYynt27Uc9sisJVkwameCw2ExojQEIAoVUKbg-Z8GTR}
pwn.college{nccgQfy7DqrXHmBCuEeRa9yBrMJR3QunHA-WgZVPfvIyTij}
pwn.college{JnxHu9ib2HtpSQ7b04o8bgHcAgVP0e6flVesMpIZGLmr5ON}
pwn.college{p4jBYDFkVk0.72GMHyZRXYY83eJbcnRYlfAxN96J.9jT1js}
pwn.college{4bAeoxGhysNIR2LR4Kcxg24MLnXW51TIMHtzxxYTQT3PxXZ}
pwn.college{zRfClf92gsWTXP.SeUN8oBeBvuNtIMsPprsMwhmT-2PlLIV}
pwn.college{tsYNLNIQRPjncwFVKRSG.AnHrG2HsyaoZ0Mkk4HAPFtnzVT}
pwn.college{wXOmU8ME2npaXNuvbM7iqEAOMxCbLSjXa0tqQSmK5m-KDrm}
pwn.college{E-H-7pYUI.6-MCheu1j-WJ6tk7b1WyEpvaFRCDUsZNovjec}
pwn.college{XYvf0g2tVQf9pj6vtBa6dPAyzJzVzltwjR1O..tZJ4ZcSFw}
pwn.college{YT.VTjJeH6gGyHmbEgbmf0c8fKjZmWEehSZr01SehxRxmwG}
pwn.college{0G-4Ax2vierUQv4k1SXyZyllBBj.tWN0tqSGhZZ46f4.GrK}
pwn.college{stFMSYPHUr.QuK0.4PpIVdXIU8z8MwlN54kfeN3I-KofLMS}
pwn.college{Se4iVs7r7.q9lpwTunWUa3j6mwVWMjDFUNaEOnWDvLzRmkX}
pwn.college{jv.24XZczEWPdQ3TjHYvggiRhainDEZul07lExCIAwUnIJk}
pwn.college{wdH8iEDpLLj3ktb6AglqtdAPwHPyv9P3.80o0Kzp5VdeIVY}
pwn.college{cLmcQmBVa6VzL.AR7FkjQNSkrRU8ESg08711ErrADxrvTSZ}
pwn.college{vS62e2EL6z8R-qKUPLU8uBc256NgG7OwcQ8g41IQRQ22UeR}
pwn.college{E30DDwJej6di2EYIe9YLQTTH5zmBffMskWxxBEFGXaDkWmD}
pwn.college{msjXw5GOZGTDp4d9VMW.fdUKxw1HCmuWyR2b5xkXzXsOg1S}
pwn.college{4OTJ480cOLiH7BvgDlsvIgk1WDaPOBu8At8VhipVzvF9zAC}
pwn.college{byD35WpNj3p1DQka8qZF682M0gET.ddkOke.0w-OU06.dtw}
pwn.college{AiBUwhco9k71m7smBOPLxjOIe7-HQiLK28oPdJknE97wEfb}
pwn.college{2A-FOR1oulOQwPRXwf3pZYBJYiLwQ6YZra5v7I1oPBFq99d}
pwn.college{mbfyD7amLvd.4rmC80hztd8ehBuHE8Xe6uOoUiBXfeoj6MO}
pwn.college{d2ho1yCSWspZXq9l-jqroDuGE73yeAfPxfGOyIZeDkimbr2}
pwn.college{CYxhn-3mzEjP5Uejwo6cjR-k2PcB-8.xO-6hwoP941mTzks}
pwn.college{0ad66SDpVpeOaa6G1eykJns38c9A0dNDvYM90Nc9GnCRxhv}
pwn.college{a8vf7Cw2BYJ7q51hlRYI-IhuaROW.wVMzJAnTL76ilnmDpM}
pwn.college{g0LEPC2kOSXUnX5mA7Lan-bK2yJM4nFEeXFdMg4ycDtBtTj}
pwn.college{Jev4UvO9qkmQu-as0DGaUkZseo6Cy-R7ROH7ZTOqGdR17zQ}
pwn.college{26a3YNNdr7ngB4Q1iwQsdQY0V-S4DmvtJvx.SrM5vXQTp4S}
pwn.college{-acJaUtTzvjEuqx7zGZe1fWJglXFtZwkGL4ZHp-TfKEbnBQ}
pwn.college{OdLNaNBvpt3DbOQZQxTuROkDCefnmoiPch.FXGq293kenc1}
pwn.college{xRHh0Ji.OEE.BZUvUeTGjGRubPvZgAt0CGWOtzGy7JXIieK}
pwn.college{NjB5jRqNCFsuxdE34WdlC8n2UbLCnQSc1IPIm6MTcW0dJIa}
pwn.college{d4ddm6IGLKQhneq.RvM3Ua9VI07jvz.uCy0PbaA0K--4SlJ}
pwn.college{hAi20EmxS3V6rjs.kKRiKHxOSCRVDvrm77FDRIkpPFcWx6h}
pwn.college{Aube1-0l5C9vPkVoByzsBpeThRFP7cE-MpEavijdyF2c27G}
pwn.college{oZpou2uJeqEn11KGGRvU6CZa7RRjuZAvLEI9YgyoN3GmrwD}
pwn.college{c49oegW0q8vBTUL64DKKTHSJ4VL8XL2ksFpUCW1muq1NpbG}
pwn.college{r7tVD0DqFmX-kTHhmkbF5rKdtDWlZb3sHBh8tGy-v1dXoTE}
pwn.college{cBppDq0C8dGVvMRi9LmTDUDFLElUBjt5hoPbF7QJ0pSB48j}
pwn.college{ALW7hRos1ESqmWgPlNSKjf48Ca-jelZQzFFoxjxJYWSIDP9}
pwn.college{6qoSNbHI29As5ZLppEqq-s-LXHXU340IMd8uJOUS-24IiKl}
pwn.college{n17ckQ5NAYwLmhRamw5-hCG8lsHy4.80xANxhQ1BprCYrsw}
pwn.college{UWlECvBlU9usznJKFhGqaADWTl.HqCyPjiXwJlusDaw8gUj}
pwn.college{clciXd5Fdg4EoqIG7LHEWOySNILasPQt9Dd7swj9t45CG.x}
pwn.college{ujOp8De4s64ZVeTQlG.-mUR6TcJEL-WZTYo9Uj-kAFVpJtF}
pwn.college{.z9F1SAMKHWFhgBqVtb99.pdteWyr9IaSBJVbwLssMP.kV9}
pwn.college{cxcoUFY8tBIrYgOOMXRDfGBIUIG0M4jqRnO8iK5b3Qn-.Z5}
pwn.college{x0RhEt4fQ35x8t9YBxnNdiVo0.LK9aJQDnzHjhJ1siC2cyh}
pwn.college{LjGBPAljQnogWgrb48tdPvMdM0Vh.C.Mo4a1tQwmUxxoh9Q}
pwn.college{gDpLK9e1AZa2ukAnDUR4VyjRz79oL8-cGyA068h557Xv9F4}
pwn.college{.ANJ4uJru-FSPGLNLqwMXiufP4lyMqSQknqdaZ6K5I-dQFe}
pwn.college{-ViDXqNDR7msAXxObCf7fdZKSDh1uYq4Pz2g3ylgeVBf9rJ}
pwn.college{1qRayFkg3V9jt2qCyJeuUtmrgCAURk.-8p3bdxkXTFN0tcI}
pwn.college{hrklHVToFhkoHSAYpu2zaI8tqDZpt5NaQnZmR.651o0Ebvl}
pwn.college{lGZPzPBfTyimxxWZzCWwct7o6qvxnxE9LZ4WouKb019lxN7}
pwn.college{vTnz-7ZJ93Xcx5K7ZCw.akouVfrQJpCBtoBDhs.00vVzAGX}
pwn.college{yzVeWcs-PhqdrFpB7wG-hqfnxX-PA6PMKTlspbhGVHScV0A}
pwn.college{tsXXaceRewdqFkpd8jKyo.Ww-0melxSDr7.OteO5Znx3wOF}
pwn.college{O-poTMm3tapwmY558O7vAINUno70AmaTQSiEWL3Fx1j4uN4}
pwn.college{ge406QOSLzrNMqqk9Dv4keit8a7exIZIyjm-qsG4yqdMTst}
pwn.college{PWJwimRCAXe9QYFajNl0NWN8GtT.ZrfJnZhXwLv4HCvlkx2}
pwn.college{30TbGAAbL8XKPe3dbwUFHbdi-hUJoGPPzsiqH8tA0aO9NyV}
pwn.college{JcyJd5bY4iVtrxpdgXQ3QqSN0khzkLhqMiQs3ksPYNWo8xW}
pwn.college{okftMCSwFZ.erCQed45u93w0fq0MEej-8HsPqIUBQCwQeAd}
pwn.college{3ey-NRErNqv..Ik5B2JuhXQ.1nCqaMa6AKoROwuH1PMzFuX}
pwn.college{8uEJisRMnbE2JT2OsJ4gfFdVqUTtFxC4SIzmDvF--LXawH.}
pwn.college{0izeUyOYFgfrl6ybFcQZtBkuBD2o7gZei7aLciPUwdR9T6E}
pwn.college{Zt4w417WLg-tbdIXJ6RMUPUGzvO52dZDraA9JothUkGq.PP}
pwn.college{Yd17r1su-AipRqooz17zyn..OBbpjbd6rjhbi2oOoUD3fq3}
pwn.college{h1L9Zz74K8s72ZgnBPp67QfbmvFyQjRwvsnmizUJ1i9Vudp}
pwn.college{3jSSamurPzhIZ3G4g5s1ldhsKJfQBWfsymJEf96iwXt1AFJ}
pwn.college{qEt7wAfUpDb-QqPDJH0UpPfsDaPqDvw3frQcaFzyxM8JaaA}
pwn.college{AgWYuhe5289-Yq1EanrWxM9quqetfDDPYrtsl111geB6NtT}
pwn.college{6HQnZbXGgWPJ11kSr-sSNE1cq5sLiTEvhuVUlMA4imXt8Si}
pwn.college{e2olmFCs14fjsBIivhxHFDx2e3Kvboo5oBe88wNPA3ddUWn}
pwn.college{HVtMLcJ33Q5Kqy22uuKDxipovkfwS3BFr9PJsMK2SE-murP}
pwn.college{x0EYxkEnJ7x07OY2OmISbGyrjXLT82iiNU8g6xZ0n9deYls}
pwn.college{BdxRMpa3FYBJYciSv1eV2F8ZJwCR4alKHViT5lIQa3aARX5}
pwn.college{kzA46vBRBzV4vwUv25y6ScTCPrYttl1KmJ6nHIMYe7i2ygb}
pwn.college{gVH4zU1ewNAgBrxOYaSmfaReCA7XHPUHwu.O999TwQgjB.m}
pwn.college{9c59A84QCauZg1cqoF..z49iHb.HRCi8-jiYu1s7PZordwF}
pwn.college{xy26gVhR799QTibeSqxBOXnir1UDpdAQ8WqVcZJ.-aCF2ds}
pwn.college{AzQKDVdPpWOPbINS.MoHF0zau6zMIzxNB42bNIWSnFrf2HH}
pwn.college{zdZqBzHtLuDgwSY9MNmQKhuhiSiV3fAu2obYmPsDapj5GKm}
pwn.college{UWS77-PnUImNjsJfwELQvp466zgzr6ANe2..2hpCh5SuKF1}
pwn.college{dE6600AD46eoE4VuTCHS.6mz27.7xP8nhOprCmv0-913JlW}
pwn.college{YtPCy6YBtUrUfw49TOSH2T5ymR2U80Epo6RO04T2QOeCZS5}
pwn.college{k0Bw1GqeIkRuHh2BiJUD6PTCZY.eCJFfde7Xlw4JYQgQ1Y.}
pwn.college{OpVGsVo-bra.qNGMmBqwB91tJocRXAqkOpnXver0UcsdzH8}
pwn.college{wu2.mXZjd1Ac5y.reUiNirIyrhrpEKb2S5ch8dF-7T8Ztyy}
pwn.college{IsIgx5uLfqQUxPfM4DXowMkkdlg-oAYTij3T.uPfjzkyqDX}
pwn.college{05kK.bpz9xReg0YilV3FevMIsyUWMjeu5NVtvXOcaQACGyj}
pwn.college{Cqg55-5L5IiaLGX3dTMlZYSqw6T6YASVOLcy1.oMw5mYBI9}
pwn.college{JZjLDsXFObHDbsHOs.YK-bTB41o6EaurB7mtXeCwZ0I8Qcj}
pwn.college{SlHFYQp9AM97dgWK8D8FTGIqL01bYMtN2JzkaGbbMu4Y7nJ}
pwn.college{6Vkz0F0mNe6THAGv5rlb95HdRvcldxyuDv9E4V5fXif6j3H}
pwn.college{Y6dGTPgxrceDnMhV1Xm55Njs2zKQmds6eAEEd7IzwKpSMVp}
pwn.college{UBcTVP-7S5W91bBEcOYLJ3Fbx3AxYEKETEeC-YwXLlLQA3R}
pwn.college{wzRe9tkcOR0VR9YmLJEiMjKeDfV8upx1r08S6TM0zHEvMIP}
^C
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{ct85ze07RMMs5DCSBYyeO3dXWN2.0FNzMDOxwyN5EzNzEzW}

# Reference
None.
