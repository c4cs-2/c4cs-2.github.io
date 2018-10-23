---
---
## **curl**
---
---
`curl` is a useful tool to transfer files to and from a server

## Basic Use
---
```
$ curl [url]
```

curl is built on libcurl and supports a ton of protocols:

>DICT, FILE, FTP, FTPS, GOPHER, HTTP, HTTPS, IMAP, IMAPS, LDAP, LDAPS, POP3, POP3S, RTMP, RTSP, SCP, SFTP, SMB, SMBS, SMTP, SMTPS, TELNET and TFTP\

<!--more-->

## Useful Options
---

making a post to the server:

```
-d [content]
```

including header info (e.g., content type):

```
-i
```

saves output in file

```
-o [file]
```

downloads the file:

```
-O 
```

delete something on the server:

```
-X DELETE [file] 
```

follow a redirected URL (a URL that has moved elsewhere):

```
-L
```

## **Protection**
---

Authentication is important to prevent access to the serving using curl. curl supporls the following:


```
curl -u username:password ...
```

## **Play Around & Reference**
---

This turotial was written with the help of [Traversy Media's 
"Basic cURL Tutorial"](https://www.youtube.com/watch?v=7XUibDYw4mc).

This video encourages using curl and playing around with [this site](https://jsonplaceholder.typicode.com/), which is an online Rest API.

## Happy curling!