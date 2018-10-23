---
---

expand
---
`expand` converts tabs into spaces within a file.

~~~ bash
$ cat file1
This    Is      Tabbed$
$ cat -A file1
Tabbed^IFile^IHereI^$
$ expand file1 > file2
$ cat -A file2
This    Is      Tabbed$
~~~

<!--more-->

### Useful Options / Examples

#### `expand -i, expand --initial`
Prevents conversion of tabs after non-blanks,

~~~ bash
$ cat 1
	    Tabs Before         After
$ cat -A 1
^I^ITabs Before^I^I^IAfter$
$ expand -i 1 > 2
$ cat 2
        Tabs Before			After
$ cat -A 2
        Tabs Before^I^I^IAfter$
~~~

#### `expand -t, expand --tabs=N`
Expand by default converts tabs into a certain number of spaces.
Using the `expand -t` option allows a different number of spaces(N) to be converted.

~~~ bash
$ echo "With expand -t"
With expand -t
$ cat -A 1
Another^ITabbed^IMonstrosity$
$ cat -t3 1 > 2 
$ cat -A 2
Another   Tabbed   Monstrosity$
~~~

~~~ bash
$ echo "With expand --tabs=3"
With expand --tabs=3
$ cat -A 1
Another^ITabbed^IMonstrosity$
$ cat --tabs=3 1 > 2 
$ cat -A 2
Another   Tabbed   Monstrosity$
~~~

#### `unexpand`
Used to convert space characters (blanks) into tabs in each file.

~~~ bash
$ cat -A 1
These     Are     Spaces    Yay$
$ unexpand 1 > 2
$ cat -A 2
These^I  Are^I  Spaces    Yay$
~~~


#### `expand --help`
Displays help message and exit

~~~bash
Usage: expand [OPTION]... [FILE]...
Convert tabs in each FILE to spaces, writing to standard output.

With no FILE, or when FILE is -, read standard input.

Mandatory arguments to long options are mandatory for short options too.
  -i, --initial    do not convert tabs after non blanks
  -t, --tabs=N     have tabs N characters apart, not 8
  -t, --tabs=LIST  use comma separated list of tab positions
                     The last specified position can be prefixed with '/'
                     to specify a tab size to use after the last
                     explicitly specified tab stop.  Also a prefix of '+'
                     can be used to align remaining tab stops relative to
                     the last specified tab stop instead of the first column
      --help     display this help and exit
      --version  output version information and exit

GNU coreutils online help: <http://www.gnu.org/software/coreutils/>
Full documentation at: <http://www.gnu.org/software/coreutils/expand>
or available locally via: info '(coreutils) expand invocation'
~~~

#### `expand --version`
Displays version information and exit

~~~bash
expand (GNU coreutils) 8.28
Copyright (C) 2017 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Written by David MacKenzie.
~~~