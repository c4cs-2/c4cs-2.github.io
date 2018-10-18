---
---

date
-------

`date` is a command that can display date information.

~~~ bash
$ date
Wed Oct 17 21:27:08 EDT 2018
$ TZ='PDT' date
Thu Oct 18 01:27:13 PDT 2018
~~~

<!--more-->

### Useful Options / Examples

#### `date -d "DATE"`

prints the date described by `DATE` in local time

~~~ bash
$ date -d '4/3/1995'
Mon Apr  3 00:00:00 EDT 1995
$ date -d 'now'
Wed Oct 17 21:29:41 EDT 2018
$ date -d 'next friday'
Fri Oct 19 00:00:00 EDT 2018
$ date -d 'last saturday -2 years'
Thu Oct 13 00:00:00 EDT 2016
$ date -d 'two hours ago'
Wed Oct 17 19:53:52 EDT 2018
~~~

#### `date -r FILE`

prints the time of last modification for `FILE`

~~~ bash
$ touch date.txt
$ date -r date.txt
Wed Oct 17 21:49:56 EDT 2018
~~~

#### `date -s "TIME"`

sets the clock to be `TIME`

~~~ bash
$ date -s "last saturday"
$ date
Sat Oct 13 00:00:00 EDT 2018
~~~

#### `date -u`

prints the time in UTC

~~~ bash
$ date -u
Thu Oct 18 02:05:09 UTC 2018
$ date -u -d "last saturday"
Sat Oct 13 00:00:00 UTC 2018
~~~

### Formats [+%]

#### `date +%s`

prints the seconds since 1970-01-01 00:00:00 UTC

~~~ bash
$ date +%s
1539828610
~~~

#### `date +%j`

prints the day of the year

~~~ bash
$ date +%j
290
~~~

#### `date +%A`

prints the full weekday name

~~~ bash
$ date +%A
Wednesday
~~~

#### `date +%B`

prints the full month name

~~~ bash
$ date +%B
October
~~~

#### `date +%^<format>`

prints `<format>` in capitals where possible

~~~ bash
$ date +%A,\ %^B\ %d
Wednesday, OCTOBER 17
~~~

[See the GNU man page for more details.](https://www.gnu.org/software/coreutils/manual/html_node/date-invocation.html#date-invocation)

