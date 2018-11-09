---
---

ed
-------

`ed` is a line-oriented text editor. It is used to create, display, modify and otherwise manipulate text files, both interactively and via shell scripts. Ed is the "standard" text editor in the sense that it is the original editor for Unix, and thus widely available.

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

### Useful Options / Examples
-p <string>
Specifies a command prompt. This may be toggled on and off with the 'P' command. 

-s
Suppresses diagnostics, the printing of byte counts by 'e', 'E', 'r' and 'w' commands, and the '!' prompt after a '!' command. This option may be useful if ed's standard input is from a script. 

-v
Verbose mode; prints error explanations. This may be toggled on and off with the 'H' command.

#### Example command
$ ed -p\*
*a
This is a line of text
This is another line of text
We can keep making lines of text all day 
.
*w ed.txt

##### Break it down
First we are activating ed from bash with a command prompt of '*', then we enter the command a to begin writing to the buffer. We enter three lines of text, then end it with a line that is only a period. Now our asterisk comes back and we write the current buffer to a file 'ed.txt'. The number of bytes in the buffer are outputted on the command line and the file 'ed.txt' now contains our three lines of text.

#### Example command
$ ed -p\*
*a
Line one
Line two
Line three
Line four
Line five
.
*3,5W ed.txt

##### Break it down
Similar to the first example, we start the editor and create a buffer. After our buffer is created, we specify a range of line three to line five and append with 'W' to the filename specified. So what this command is essentially doing is appending lines 3-5 of our buffer to the end of the file ed.txt
