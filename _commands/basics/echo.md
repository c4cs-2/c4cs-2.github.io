---
---

echo
----

`echo` allows you to send a line of text to standard output.

~~~ bash
$ echo "Hello World!"
Hello World!
~~~

<!--more-->

### Useful Options

`-n` will stop `echo` from outputting a trailing newline.

`-e` will enable interpretation of backslash escapes. See below for examples
of recognized escape sequences.

`-E` will disable interpretation of backslash escapes. This is the default.

### Some Recognized Escape Sequences

| Sequence  | Character |
| :------:  | :-------- |
| `\\`      | backslash |
| `\n`      | new line |
| `\r`      | carriage return |
| `\t`      | horizontal tab |
| `\v`      | vertical tab |

### Example Commands

Using the `-e` option allows inclusion of escape sequences.

~~~ bash
$ echo -e "I love writing text on\nmultiple lines and\tusing tabs."
I love writing text on
multiple lines and      using tabs.
~~~

Echo can be used to write to a file using output redirection:

~~~ bash
$ touch myfile.txt
$ echo "This is some text for my file." > myfile.txt
~~~
