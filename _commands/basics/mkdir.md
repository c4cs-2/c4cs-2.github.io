---
---

mkdir
-------

`mkdir` is a basic command for making directories.

~~~ bash
$ mkdir newDirectory
$ cd newDirectory
~~~

<!--more-->

### Useful Options / Examples

### `mkdir -p`

The `-p` or `--parent` option creates any parent directories necessary for the new directory.

~~~ bash
$ #/a directory does not exist
$ mkdir -p /a/b
$ #both /a and /a/b created
$ mkdir -p /a/c
$ #since /a exists, only /a/c was created
~~~

### `mkdir -m`

The `-m` or `--mode` option allows you to set the permission mode of the new directory as
you create it.

~~~ bash
$ mkdir -m 777 a
$ #created directory a with permissions rwxrwxrwx
$ mkdir -m 700 b
$ #created directory b with permissions rwx------
~~~

### `mkdir -v`

The `-v` or `--verbose` option will make the command output a message for each directory made.

~~~ bash
$ mkdir -v a
mkdir: created directory 'a'
~~~

