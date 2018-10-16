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

### `cmp -l`

Prints byte position and differing byte values

~~~ bash
$ cmp -l file1.txt file2.txt 
20   12   56
21  124   12
22  150  124
23  151  150
24  163  151
25   40  163
26  146   40
27  150  151
28   12   24
29  124  145
30  157  163
~~~

### `cmp -s`

Supresses the output of the command, and prints 0 for identical and 1 for different

~~~ bash
$ cmp -s file1.txt file2.txt 
1
~~~

### `cmp -n`

Allows the user to compare a certain number of bytes

~~~ bash
$ cmp -n 50 file1.txt file2.txt 
~~~
