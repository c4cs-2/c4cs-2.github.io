---
---

**Command:** *whoami*
-------

**Description:** "whoami" is the concatenation of the strings "who" + "am" + "i". 
The command is as easy as it sounds, printing out the user name associated with 
the current effective user ID. whoami is particularly useful when using shells 
such as ash and sh that do not show the name of the current user in the command prompt.

~~~ bash
foo@bar:~$ whoami
foo
~~~

<!--more-->

### Useful Options / Examples

**Example 1**
~~~ bash
gfolbe@DESKTOP:~$ whoami
gfolbe
~~~
**Description 1:**
gfolbe is the logged in user. This can be seen by looking at what comes before 
the @ sign. The only action that occurs here is that gfolbe is printed out. 
It should be understood that the logged in user is not always visible. If this
is the case, the whoami command will still execute as it should.

**Example 2**
~~~ bash
gfolbe@DESKTOP:~$ whoami --help
Usage: whoami [OPTION]...
Print the user name associated with the current effective user ID.
Same as id -un.

      --help     display this help and exit
      --version  output version information and exit

GNU coreutils online help: <http://www.gnu.org/software/coreutils/>
Report whoami translation bugs to <http://translationproject.org/team/>
Full documentation at: <http://www.gnu.org/software/coreutils/whoami>
or available locally via: info '(coreutils) whoami invocation'
~~~
**Description 2:**
A help message is printed out that explains what the command is used for
