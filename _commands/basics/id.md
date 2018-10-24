id
=====

`id` is a command that shows the real and effective user and group IDs.

Usage
------
example: `$ id myusername`

output:
```
uid=1000(myusername) gid=1000(myusername) groups=1000(myusername),4(adm),20(dialout),24(cdrom),
25(floppy),27(sudo),29(audio),30(dip),44(video),46(plugdev,108(lxd),114(netdev)
```

Flags and Arguments
-------------------
  * `-G` to print only group ids
  * `-g` to print only effective group id
  * `-u` to print only effective user id
  * `-r` to print real ids instead of effective ids (can be paired with other flags)
