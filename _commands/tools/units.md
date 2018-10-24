---
---

units
---
`units` is a unit converter and calculator.

~~~ bash
$ units

You have: 100 feet
You want: meters
	* 30.48
	/ 0.032808399

You have: 12 gallons
You want: liters
	* 45.424941
	/ 0.022014338
~~~

<!--more-->

### Using `units`:

On giving the command `units` in your terminal, you are prompted with:

~~~ bash
You have: 
~~~

You should then provide either a measurement (`8 liters`) or just the units (`meters`, which is the same as typing `1 meter`). You are then prompted with:

~~~ bash
You want:
~~~

You should then provide the units (`feet`, `gallons`, etc.) to which you want the measurement you provided before converted.

If the units provided were compatible (it can't convert `miles` to `milliseconds`!), you will then receive two lines of output; the first will be the answer you are probably looking for, and the second will give the inverse of the factor used to convert between the two units.

### Example:

~~~ bash
$ units

Currency exchange rates from finance.yahoo.com on 2017-10-31 
3045 units, 109 prefixes, 109 nonlinear units

You have: 100 feet
You want: meters
	* 30.48
	/ 0.032808399
~~~

The first line demonstrates that there are 30.48 meters in 100 feet. The second line demonstrates that one meter is .032808399... times the size of 100 feet.

Different messages are displayed when units aren't compatible, when you had `units` perform a reciprocal conversion, etc.

### More Information:
More information on using `units` can be found in its original [manual](https://www.gnu.org/software/units/manual/units.html).
