---
---

export
-------

`export` marks an environment variable to be exported with any newly forked child processes.

~~~ bash
$ export MYENV=EECS398
$ export -p | grep MYENV
declare -x MYENV=EECS398“
~~~

<!--more-->

### Useful Options / Examples

### `export -p`
`export -p` can enable us to to view all exported variables on current shell.




### `export EDITOR=/usr/bin/vim`
`export EDITOR=/usr/bin/vim` can set vim as a text editor.

~~~ bash
$ export EDITOR=/usr/bin/vim
$ export | grep EDITOR
declare -x EDITOR="/usr/bin/vim"
~~~


### `export -n [varName]`
To remove names from exported list, use `-n` option.

~~~ bash
$ export -n EDITOR
$ export | grep EDITOR

~~~

No output after grepping all exported varables, as EDITOR exported variable is removed from exported list.




### `export -f [functionName]`
To export shell function, use `-f`option.

~~~ bash
$ functionName () { echo "print this line"; }
$ export -f functionName
print this line
~~~



