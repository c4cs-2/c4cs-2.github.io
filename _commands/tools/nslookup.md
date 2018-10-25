---
---

nslookup
-------

Displays information that you can use to diagnose Domain Name System (DNS) infrastructure.

~~~ bash
nslookup [domain name]
~~~

This will return a response that gives the server and address of the domain name.

### Useful Options / Examples

#### Example command
~~~ bash
nslookup microsoft.com
Server:     8.8.8.8
Address:    8.8.8.8#53
~~~
##### Break it down
This is the response from the command, the 8.8.8.8 is the address of the domain name and the "#53" is referring to port 53, which is the standard port number domain name servers use to accept queries.
#### Example command
~~~ bash
nslookup 134.170.185.46
Server:     8.8.8.8
Address:    8.8.8.8#53
~~~
##### Break it down
This previous command is known as a reverse nslookup command. This means that you provide the IP address as opposed to the domain name, however it returns information in the same format as a regular nslookup (i.e. a non-reverse nslookup command)
