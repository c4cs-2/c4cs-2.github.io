---
---

emacs
---
`emacs` is a text editor characterized by its customizability and large number of useful commands.

<!--more-->

## Basic Commands

#### `emacs <filename>`

Opens *filename* in emacs

~~~bash
$ emacs filename
~~~

#### `Ctrl-x Ctrl-c`

Exits emacs. You will be prompted to save or discard your changes

#### `Ctrl-x Ctrl-s`

Saves changes without exiting

## Cursor Movement

`Ctrl-b`: go backwards one character without deleting it

`Ctrl-f`: go forward one character without deleting it

`ESC b`: go backwards one word

`ESC f`: go forward one word

`Ctrl-p`: go up one line

`Ctrl-n`: go down one line

`Ctrl-a`: go to beginning of line

`Ctrl-e`: go to end of line

`ESC <`: go to beginning of file

`ESC >`: go to end of file

`ESC x <line-number>`: go to line specified

## Editing Text

*Note: 'kill' refers to the operation of removing a piece of text and putting it into the 'kill ring', from which it can be 'yank'ed back into the file.This is similar to cutting and pasting in other applications.*

`DEL`: delete previous character

`CTRL-d`: delete next character

`ESC DEL`: kill previous word

`ESC d`: kill next word

`ESC 0 CTRL-k`: kill line to beginning

`CTRL-k`: kill line to end

`CTRL-y`: yank most recent killed text

`CTRL-<SPACE>`: set mark at cursor and activates mark, allowing you to move your cursor to select a block of text

`CTRL-w`: kill marked block

## Search

`CTRL-s`: incremental search forward

`CTRL-r`: incremental search backward

## Macros

`CTRL-x (`: start defining macro

`CTRL-x )`: end macro definition

`CTRL-x e`: executes last defined macro

`CTRL-x CTRL-k <key>`: binds last defined macro to the key specified
