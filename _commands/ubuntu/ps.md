---
---

ps
---

`ps` is used to list running processes in the shell

~~~ bash
$ ps
~~~

<!--more-->

### Useful Options / Examples
There are many options, most handling the way the processes are selected:

### `ps [options]`

The four items are labeled PID, TTY, TIME and CMD. 
PID: Process Identification Number (unique identifier for each process)
TTY: Terminal Type (name of the terminal that the user logged into
TIME: The amount of CPU time in minutes and seconds that the process has been running
CMD: The name of the command that launched the process

~~~ bash
$ ps 
PID  TTY   TIME     CMD
2154 pts/0 00:00:01 bash
2240 pts/0 00:00:00 ps
~~~

### `ps -x` 

`-x` option shows the processes that have no controlling terminal, like *daemons*

~~~ bash
$ ps -x
~~~


### `ps -aux | less`

This is a common and convenient way to obtain more information about all current processes


###  `More Process Selection:`
	-A 	select all processes
	-d	select all, but omit session leaders
	-N	negate selection
	r	restict output to running processes
	T	select all processes on this terminal
	-C	select by command name
	-G	select by RGID
	-p	select by PID
	-s	select by Session ID

There are of course many more, but these should be enough to suffice for most needed operations

































































































































































































































































































































































