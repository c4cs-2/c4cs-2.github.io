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


