---
---

ifconfig
---
`ifconfig` is a command used to view and change of the configuration of the network interfaces on your system.

~~~ bash
$ ifconfig
~~~

<!--more-->

### Useful Options / Examples

### `ifconfig` no flags

Displays information about all network interfaces currently in operation.

~~~ bash
$ ifconfig
enp0s3: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.0.2.15  netmask 255.255.255.0  broadcast 10.0.2.255
        inet6 fe80::e012:7028:78b7:cec  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:13:37:c4  txqueuelen 1000  (Ethernet)
        RX packets 194514  bytes 212448974 (212.4 MB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 55184  bytes 3440644 (3.4 MB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 1198  bytes 16561376 (16.5 MB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 1198  bytes 16561376 (16.5 MB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
~~~

Here, *enp0s3* and *lo* are the names of the interfaces.

### `ifconfig <interface>`

Displays information about the interface named `<interface>`

~~~ bash
$ ifconfig epn0s3
enp0s3: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.0.2.15  netmask 255.255.255.0  broadcast 10.0.2.255
        inet6 fe80::e012:7028:78b7:cec  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:13:37:c4  txqueuelen 1000  (Ethernet)
        RX packets 194907  bytes 212501702 (212.5 MB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 55571  bytes 3479269 (3.4 MB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
~~~

### `ifconfig -a`

Produces the same information as when running `ifconfig` except it includes interfaces that are not currently active. 

### Enabling and Disabling Interfaces

To enable or disable an interface, the keyword `up` or `down` respectively can be added after the interface name. For this command to work, the user must have superuser permissions so you must be logged in as root or prefix the command with sudo.

~~~ bash
$ sudo ifconfig enp0s3 up
~~~

~~~ bash
$ sudo ifconfig enp0s3 down
~~~

### Configuring Interfaces

You can configure interfaces by assigning static IP addresses, network masks, and broadcast addresses to the interfaces. As when using the keywords `up` and `down`, you must be a superuser to run these commands. These commands can be done separately, or they can be done all together. (Note: you cannot assign a dynamic IP address with `ifconfig`.)

~~~ bash
$ sudo ifconfig enp0s3 216.3.128.12 # This assigns a static IP address
$ sudo ifconfig enp0s3 netmask 255.255.255.0 # This assigns a network mask
$ sudo ifconfig enp0s3 broadcast 192.0.2.1 # This assigns a broadcast address
$ sudo ifconfig enp0s3 216.3.128.12 netmask 255.255.255.0 broadcast 192.0.2.1 # This assigns a static IP address, a network mask, and a broadcast address to enp0s3
~~~


