---
---

rm
---
`rm` stands for "remove" and is used to remove objects such as files, directories, symbolic links, ...etc

~~~ bash
#
$ rm a.txt
$ rm b.txt c.txt
$ rm -i d.txt
remove d.txt? n
$ rm -i d.txt
remove d.txt? y

~~~

<!--more-->

### Useful Options / Examples

### `git init`

Initializes the current directory as a git repository

~~~ bash
$ git init
~~~

### `git status`

`git status` shows the current state of your git repository. This lists the current branch, all the
changes that have been made, and which changes are being tracked.

~~~ bash
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	modified:   hello.cpp

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   bye.cpp

~~~
