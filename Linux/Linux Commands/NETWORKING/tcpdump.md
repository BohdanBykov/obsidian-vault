***
### About:
Command that can listen packets that go throw network interfaces.
https://danielmiessler.com/study/tcpdump/

***
### Use Cases:
- #### use to show available interfaces
```sh
╭─bohdan@fedora 
╰─$ sudo tcpdump -D
1.wlp4s0 [Up, Running, Wireless, Associated]
2.any (Pseudo-device that captures on all interfaces) [Up, Running]
3.lo [Up, Running, Loopback]
4.enp3s0 [Up, Disconnected]
5.bluetooth0 (Bluetooth adapter number 0) [Wireless, Association status unknown]
```

 - #### use to listen wlp4s0
```sh
╭─bohdan@fedora ~ 
╰─$ sudo tcpdump -i wlp4s0
dropped privs to tcpdump
tcpdump: verbose output suppressed, use -v[v]... for full protocol decode
listening on wlp4s0, link-type EN10MB (Ethernet), snapshot length 262144 bytes
15:37:53.836912 IP 1.1.1.1.https > fedora.55555: Flags [.], ...
15:37:53.836912 IP fedora.55555 > 1.1.1.1.https: Flags [.], ...
```

- #### use to show packets where source is fedora(src/dst)
```sh
╭─bohdan@fedora ~ 
╰─$ sudo tcpdump -i wlp4s0 src host fedora                                                                                                                          
dropped privs to tcpdump
tcpdump: verbose output suppressed, use -v[v]... for full protocol decode
listening on wlp4s0, link-type EN10MB (Ethernet), snapshot length 262144 bytes
15:39:53.83914 IP fedora.55555 > 1.1.1.1.https: Flags [.], ...
15:39:53.83979 IP fedora.55555 > 1.1.1.1.https: Flags [.], ...
```

- #### use to show packets where port is 443
```sh
╭─bohdan@fedora ~ 
╰─$ sudo tcpdump -i wlp4s0 src host fedora and port 443   
dropped privs to tcpdump
tcpdump: verbose output suppressed, use -v[v]... for full protocol decode
listening on wlp4s0, link-type EN10MB (Ethernet), snapshot length 262144 bytes
16:25:49.568770 IP fedora.5555 > domainname.net.https: UDP, ...
16:25:49.569096 IP fedora.5555 > domainname.net.https: UDP, ...
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
