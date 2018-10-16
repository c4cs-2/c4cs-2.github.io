---
---

stat
-------
Displays information about a particular file or a filesystem
```
$ stat stat.md
16777220 8601693068 -rw-r--r-- 1 [user] staff 0 0 "Oct 16 09:53:40 2018" "Oct 16 09:53:36 2018" "Oct 16 09:53:40 2018" "Oct 16 09:53:36 2018" 4194304 0 0 stat.md
```
**Useful Commands:**
`-x` Display information in a more readable format
```
$ stat -x stat.md
  File: "stat.md"
  Size: 284          FileType: Regular File
  Mode: (0644/-rw-r--r--)         Uid: (  501/    jlee)  Gid: (   20/   staff)
Device: 1,4   Inode: 8601693068    Links: 1
Access: Tue Oct 16 10:08:36 2018
Modify: Tue Oct 16 09:59:27 2018
Change: Tue Oct 16 10:08:20 2018
```
`-t` Display information in terse form of output, making it easier for other programs to parse the output
```
$ stat -t stat.md
747049792 715 crw--w---- 1 [user] tty 268435461 0 "stat.md" "stat.md" "stat.md" "stat.md" 131072 0 0 (stdin)
```
`-f` Displays the filesystem status instead of a single file status
```
$ stat c4cs-2.github.io
16777220 8601691765 drwxr-xr-x 30 jlee staff 0 960 "Oct 16 10:25:39 2018" "Oct 16 09:58:18 2018" "Oct 16 09:58:18 2018" "Oct 16 09:46:29 2018" 4194304 0 0 c4cs-2.github.io

```
`--help`
```
displays possible commands and exits
```
`--version`
```
output version information of `stat` and exits
```