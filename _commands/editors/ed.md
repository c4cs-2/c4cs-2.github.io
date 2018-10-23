### 'ed'

`ed` is a line-oriented text editor. It is used to create, display, modify and otherwise manipulate text files, both interactively and via shell scripts. A restricted version of ed, red, can only edit files in the current directory and cannot execute shell commands. Ed is the "standard" text editor in the sense that it is the original editor for Unix, and thus widely available. For most purposes, however, it is superseded by full-screen editors such as GNU Emacs or GNU Moe. I've listed some basic commands below, but you can also use line ranges, move and copy text, search, substitute, read and write, and even use regular expressions

~~~ bash
# To open up the editor
$ ed
# To open up the editor with a command prompt '*'
$ ed -p\*
# To start making text, line by line
*a
# To stop making new text
*.
# To write current buffer to a file
*w filename.txt
~~~
