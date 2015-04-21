# Introduction #

As Counter Seczone I hereby mean the seczone block at

0xa03fac88.

This block contains the nck attempt counter and the

locks status.

Is useless to say that you can't just put "unlocked" bytes there

without the hash of the lock code in the a03fa400 zone.

So, let's have a look at the counters!


# Details #

This is the unencrypted "counter zone" in 3 different situations:

1) Virgin state.

2) After one NCK attempt.

3) After TWO NCK attempts.

4) After IPSF.

```
NCK Counter=0 (Virgin)
 
[0000]  [00]01[05]00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0010]   00 00 00 00 01 00 00 00   01 01 05 01 00 00 00 00   ........ ........
[0020]   09 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0030]   09 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0040]   05 05 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0050]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0060]   00 00 00 00 00 00 00 00   05 05 00 00 00 00 00 00   ........ ........
[0070]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0080]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0090]   05 05 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[00a0]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[00b0]   00 00 00 00 00 00 00 00   05 05 00 00 00 00 00 00   ........ ........
[00c0]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[00d0]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
 
NCK Counter=1 (Fucked for the first time) :)
 
[0000]  [01]01[05]00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0010]   00 00 00 00 01 00 00 00   01 01 05 01 00 00 00 00   ........ ........
[0020]   09 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0030]   09 00[01]00[01]00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0040]   05 05 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0050]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0060]   00 00 00 00 00 00 00 00   05 05 00 00 00 00 00 00   ........ ........
[0070]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0080]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0090]   05 05 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[00a0]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[00b0]   00 00 00 00 00 00 00 00   05 05 00 00 00 00 00 00   ........ ........
[00c0]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[00d0]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
 
NCK Counter=2 (Gangbanged) :)
 
[0000]  [02]01[00]00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0010]   00 00 00 00 01 00 00 00   01 01 05 01 00 00 00 00   ........ ........
[0020]   09 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0030]   09 00[02]00[07]00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0040]   05 05 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0050]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0060]   00 00 00 00 00 00 00 00   05 05 00 00 00 00 00 00   ........ ........
[0070]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0080]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0090]   05 05 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[00a0]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[00b0]   00 00 00 00 00 00 00 00   05 05 00 00 00 00 00 00   ........ ........
[00c0]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[00d0]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
 
AFTER IPSF (cumshot party)
 
[0000]  [02]01[01]04*00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0010]   00 00 00 00 01 00 00 00  *05*05 05 01*00 00 00 00   ........ ........
[0020]   09 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0030]   09 00[00]00[00]00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0040]   05 05 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0050]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0060]   00 00 00 00 00 00 00 00   05 05 00 00 00 00 00 00   ........ ........
[0070]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0080]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[0090]   05 05 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[00a0]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[00b0]   00 00 00 00 00 00 00 00   05 05 00 00 00 00 00 00   ........ ........
[00c0]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
[00d0]   00 00 00 00 00 00 00 00   00 00 00 00 00 00 00 00   ........ ........
```