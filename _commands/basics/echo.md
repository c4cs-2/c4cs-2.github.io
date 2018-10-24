---
---

echo
----

Send a line of text to standard output.

~~~ bash
$ echo "Hello World!"
Hello World!
~~~

### Useful Options

| `-n` | do not output the trailing newline |
| `-e` | enable interpretation of backslash escapes |
| `-E` | disable interpretation of backslash escapes (default) |

### Some Recognized Escape Sequences

| `\\` | backslash |
| `\n` | new line |
| `\r` | carriage return |
| `\t` | horizontal tab |
| `\v` | vertical tab |

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
