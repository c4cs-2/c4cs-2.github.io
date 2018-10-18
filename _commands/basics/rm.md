---
---

rm
---
`rm` stands for "remove" and is used to remove objects such as files, directories, symbolic links, ...etc

~~~ bash
# Format: rm [options] <filename>
$ rm a.txt
$ rm b.txt c.txt
$ rm -i d.txt
remove d.txt? n
$ rm -i d.txt
remove d.txt? y

~~~

<!--more-->

### Useful Options / Examples

### `rm <filename(s)>`

Removes the file(s) with the specified file names

~~~ bash
$ ls
a.txt b.txt c.txt d.txt
$ rm a.txt # remove a.txt
$ ls # now a.txt is not in the directory anymore
b.txt c.txt d.txt
$ rm b.txt c.txt # you can also remove multiple files
$ ls
d.txt
~~~

### `rm -i <filename>`

The `-i` flag indicates an "interactive deletion" in which the terminal will confirm with the user before deleting each file. It will only delete files if the user types *Yes*, *yes*, *Y*, or *y*

~~~ bash
$ ls
a.txt b.txt c.txt d.txt
$ rm -i a.txt b.txt c.txt
remove a.txt? n
remove b.txt? s
remove c.txt? y
$ ls
a.txt b.txt d.txt
~~~

### `rm -f <filename>`

The `-f` flag indicates an "force deletion." Normally, when we try to delete a "write protected" file (meaning that you can't write to the file) using rm command, the terminal prompt for confirmation of deletion. However, if we use the -f flag, the write protected file would be deleted immediately. 

~~~ bash
$ ls -l # showing that we can't write to a.txt b.txt c.txt
-r--r--r--+ 1 User User 0 Jan  2 22:56 a.txt 
-r--r--r--+ 1 User User 0 Jan  2 22:57 b.txt 
-r--r--r--+ 1 User User 0 Jan  2 22:58 c.txt 
$ rm a.txt # prompt may be slightly different depending on the OS
override r--r--r--  User/User for a.txt? y
$ ls -l 
-r--r--r--+ 1 User User 0 Jan  2 22:57 b.txt 
-r--r--r--+ 1 User User 0 Jan  2 22:58 c.txt 
$ rm -f b.txt # no prompts
$ ls -l
-r--r--r--+ 1 User User 0 Jan  2 22:58 c.txt 

~~~

### `rm -r <directory>`

The `-r` flag indicates an "recursive deletion." This command will all subfolders and files in the specified directory.

~~~ bash
$ ls
A B b.txt
$ tree A # shows all subfolder and files of directory A
A
├── a.txt
├── A1
│   └── a1.txt
└── A2
$ rm -r A # removes A, a.txt, A1, a1.txt, A2
$ ls
B b.txt

~~~







