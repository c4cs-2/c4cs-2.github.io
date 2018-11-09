---
---

printf
-------

printf is used to output data. You can use it in the terminal or in a bash script.

~~~ bash
$ printf FORMAT ARGUMENTS
$ printf "Here's an example of printf\n"
Here's an example of printf
$ printf "My name is %s, nice to meet you.\n" "George"
My name is George, nice to meet you.
~~~
The %s is used as a placeholder for an argument of type string.

<!--more-->

### Useful Options / Examples

#### printf multiple placeholders
~~~ bash
$ printf "I attend the %s of %s.\n" "University" "Michigan"
I attend the University of Michigan
~~~

##### Break it down
* The above example uses two placeholders within the string "I attend...". The first placeholder will be substituted with the first argument "University", and the second will be substituted with the second argument "Michigan".

#### printf with more placeholders than arguments
~~~ bash
$ printf "My %s is %s.%s%s Maybe it's time to fix that.\n" "sleep schedule" "really messed up"
My sleep schedule is really messed up. Maybe it's time to fix that.
~~~

##### Break it down
* The above example has four placeholders but only two arguments. The arguments will be substituted into the first two placeholders and the other two placeholders are ignored.

#### printf with more arguments than placeholders
~~~ bash
$ printf "Holy moly I just saw %s\n" "Jim Harbaugh" "Reggie the campus corgi" "my grades"
Holy moly I just saw Jim Harbaugh
Holy moly I just saw Reggie the campus corgi
Holy moly I just saw my grades
~~~

##### Break it down
* The above example has one placeholder and three arguments. printf will run as many times as it will take to use up all the arguments.

#### printf with more arguments than placeholders pt 2
~~~ bash
$ printf "Do you see %s and %s?\n" "that student screaming" "running away from their problems" "me fall down the stairs"
Do you see that student screaming and running away from their problems?
Do you see me fall down the stairs and ?
~~~

##### Break it down
* Like the example before it, this example has more arguments than placeholders. The first time it runs, it uses two of our three arguments. The second time running, it only has one argument left, so it ignores the second placeholder.

#### printf with different kinds of placeholders
~~~ bash
$ printf "%d\n" 500
500
$ printf "%f\n" 500
500.000000
~~~

##### Break it down
* Instead of %s, you use %d for integers and %f for floating point numbers. %f by default will print with 6 decimal places, but you can change that by specifying the number of decimal places.

#### printf with floating points with 2 decimal places
~~~ bash
$ printf "I just made $%.2f\n" "400"
I just made $400.00
~~~

##### Break it down
* In the previous example, you can ignore the $ that comes right before our placeholder (it's just the dollar sign in the string, not a separate terminal command). The % signals a placeholder. The .2 signals the two decimal places we wanted. The f specifies that the placeholder will be representing a floating point argument later. The \n sequence at the end just specifies a newline.

#### printf with special characters
~~~ bash
$ printf "Oops: %s\n" "\t"
Oops: \t
~~~

##### Break it down
* In the previous example, the placeholder %s does not allow for special characters in the arguments. The argument will be the character literals. In order to use special characters as arguments, you will need the %b placeholder instead of %s.

#### printf with special characters in the arguments
~~~ bash
$ printf "%bPushed to the right\n" "\t"
	Pushed to the right
~~~

##### Break it down
* In the previous example, we supply the string argument of a TAB character. The %b placeholder recognizes that the argument may contain special characters and will recognize the sequence.

#### Other special characters
Other special characters like quotations and backslashes can be used with the following sequences of characters:
* \" makes a double quote
* \\ makes a backslash
* \n makes a newline
* \t makes a horizontal tab
* \e makes an escape character
* \r makes a carriage return

#### For more...
~~~ bash
$ printf --help
~~~
Use the --help flag to see more information about printf.
