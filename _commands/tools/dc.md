---
---
dc 
---
'dc' (also known as "Desk Calculator") is a useful tool for doing quick calculations on the command line.

*Syntax*
---
dc uses a postfix notation:

~~~ bash
$ dc
5
10
+
p
15

10
2
*
5
+
p
25
~~~

In this example, we type the number 5 (hit enter) then type 10 (hit enter) then type "+" (hit enter). This gives us the result of 15, which we can display by typing 'p' and hitting enter. 

In the second example, we multiply 2\*10, and then add 5 to that result, leaving us with '25' as the answer when we type 'p'

### `dc -f filename`
~~~ bash
$ dc -f inFile
~~~
This example will evaluate all of the 'dc' commands found inside of 'inFile', just as if you typed them in the terminal yourself.


