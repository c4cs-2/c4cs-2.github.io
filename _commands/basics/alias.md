---
---

alias
-------

`alias` allows you to create custom temporary abbreviations for commands

~~~ bash
$ alias hello='echo "hello world!"'
$ hello
hello world!
~~~

<!--more-->

### Useful Options / Examples

#### `alias`

##### `alias` with no flags lists the current aliases in effect. This includes temprary ones created in the current terminal and system-wide aliases.

~~~ bash
$ alias
alias alert='notify-send --urgency=low -i "$([ $? = 0 ] && echo terminal || echo error)" "$(history|tail -n1|sed -e '\''s/^\s\*[0-9]\+\s\*//:s/[;&|]\s\*alerts$//'\'')"'
alias egrep='egrep --color=auto'
alias fgrep='fgrep --color=auto'
alias grep='grep --color=auto'
alias l='ls -CF'
alias la='ls -A'
alias ll='ls -alF'
alias ls='ls --color=auto'
~~~

#### `alias '<aliasname>=<command1>;<command2>'`

##### Multiple commands can be chained together under one alias by seperating the commands with a semicolon. Another alias can be used as a command.

~~~ bash
$alias 'mkfile=echo "hello world!" > file.txt;cat file.txt'
$mkfile
hello world!
$alias 'anotheralias=mkfile;echo "hello world!"'
$anotheralias
hello world!
hello wolrd!
~~~

#### `alias '<aliasname>=<command>'`

##### Previous aliases can be temporarily overwritten including permanent aliases. To disable a temporarily alias overwritting a permanent command, use a proceding backslash. This will only work for the one use. To permanently revert the alias to its previous definition is by using the unalias command.

~~~bash
$alias 'pwd=echo "I broke it!"'
$pwd
I broke it!
$/pwd
/home/user/c4csisthebest/programmingrocks/
$pwd
I broke it!
$unalias pwd
$pwd
/home/user/c4csisthebest/programmingrocks/
~~~
