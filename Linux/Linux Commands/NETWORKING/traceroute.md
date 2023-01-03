***
### About:
It is a tool that shows you throw what hosts your packets goes before destination,
also measures delays between them.

***
### Use Cases:

- #### use to explore path to google
	- -n doesn't show domain names
	- -q ping every host only one time (3 by default)
	- * means that host is unknown (but reachable)
```sh
╭─bohdan@fedora
╰─$ traceroute -n -q1 google.com                                                                                                                                         
traceroute to google.com (216.58.215.110), 30 hops max, 60 byte packets
 1  192.168.0.1  7.946 ms
 2  *
 3  89.75.24.24  18.654 ms
 4  84.116.253.98  25.468 ms
 5  *
 6  84.116.138.102  31.361 ms
 7  72.14.203.234  29.095 ms
 8  *
 9  142.250.37.209  33.482 ms
10  216.58.215.110  28.974 ms
```

 - #### use to 
```sh

```

***
### Keys:
```sh
  -4                          Use IPv4
  -6                          Use IPv6

  -I  --icmp                  Use ICMP ECHO for tracerouting
  -T  --tcp                   Use TCP SYN for tracerouting (default port is 80)

  -n                          Do not resolve IP addresses to their domain names

  -q nqueries  --queries=nqueries
                              Set the number of probes per each hop. Default is
                              3

  -s src_addr  --source=src_addr
                              Use source src_addr for outgoing packets

```

***
### Help:
```sh

```

***

