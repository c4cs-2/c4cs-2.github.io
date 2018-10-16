---
---

cmp
-------
`cmp` is a command that compares two files byte by byte to see if the files are identical or not.

~~~ bash
$ cmp file1.txt file2.txt
$ cmp file1.txt file3.txt
file1.txt file3.txt differ: byte 9, line 2
~~~

<!--more-->

### Useful Options / Examples

### `cmp -b`

Prints out the bytes that differ

~~~ bash
$ cmp -b file1.txt file2.txt
file1.txt file2.txt differ: 12 byte, line 2 is 154 l 151 i
~~~

### `cmp -i`

Skips a number of initial bytes in the comparison

~~~ bash
$ cmp -i 10 file1.txt file2.txt
~~~
