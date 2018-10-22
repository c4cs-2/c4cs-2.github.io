---
---

useradd
---
In Linux, a ‘useradd‘ command is a low-level utility that is used for adding/creating user accounts in Linux and other Unix-like operating systems. The ‘adduser‘ is much similar to useradd command, because it is just a symbolic link to it


~~~ bash
$ useradd [options] username
~~~

<!--more-->

### `How it works`
When we run ‘useradd‘ command in Linux terminal, it performs following major things:

1.It edits /etc/passwd, /etc/shadow, /etc/group and /etc/gshadow files for the newly created User account.<br>
2.Creates and populate a home directory for the new user.<br>
3.Sets permissions and ownerships to home directory.<br>

### `Add a new user`
To add/create a new user, all you’ve to follow the command ‘useradd‘ or ‘adduser‘ with ‘username’. The ‘username’ is a user login name, that is used by user to login into the system.

Only one user can be added and that username must be unique (different from other username already exists on the system).

For example, to add a new user called ‘aadhar‘, use the following command.


~~~ bash
$ useradd aadhar
~~~






