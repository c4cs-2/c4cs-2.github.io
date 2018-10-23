---
---

true
---

A function whose only purpose is to exit with a status indicating success.
Success is indicated by 0.

~~~ bash
$ true
$ echo "The previous command's exit status is $?."
The previous command's exit status is 0.
~~~
Note: $? shows the exit status of the most recently run function.

<!--more-->

### Syntax
~~~ bash
$ true [anything...]
~~~

When provided any number of arguments, including zero, true returns succesfully.

### Useful Options / Examples

#### Example 1

```
if [ true ]
then
	echo "True"
else 
	echo "False
fi
```

##### Break it down

The above example shows you that the true function works
in conditional statements and indeed returns true.

#### Example 2

```
while true
do
    /* Your code here */
done
```

##### Break it down

The above example is useful for certain control flows
where you want to keep doing something until you reach
an end condition you specify.
 
