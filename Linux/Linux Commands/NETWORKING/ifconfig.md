#  Command [[ifconfig]] :

***

## About:

### - replace [[ip]], show ip of available interfaces.

***


## Use Cases:

### - use ifconfig to show all available net interfaces 
```sh
[bohdan@fedora testdirectory]$ ifconfig
docker0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
        inet 172.17.0.1  netmask 255.255.0.0  broadcast 172.17.255.255
        ether 02:42:2d:cf:59:61  txqueuelen 0  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 0  bytes 0 (0.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

enp3s0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
        ether b4:a9:fc:f2:41:02  txqueuelen 1000  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 0  bytes 0 (0.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 2094  bytes 127958 (124.9 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 2094  bytes 127958 (124.9 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

wlp4s0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.0.172  netmask 255.255.255.0  broadcast 192.168.0.255
        inet6 fe80::7e6c:4352:9231:950f  prefixlen 64  scopeid 0x20<link>
        ether 94:08:53:89:06:a1  txqueuelen 1000  (Ethernet)
        RX packets 783889  bytes 916497777 (874.0 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 278826  bytes 221495235 (211.2 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

```

### - use to 
```sh

```


## Keys:
```sh
[bohdan@fedora testdirectory]$ ifconfig --help
Usage:
  ifconfig [-a] [-v] [-s] <interface> [[<AF>] <address>]
  [add <address>[/<prefixlen>]]
  [del <address>[/<prefixlen>]]
  [[-]broadcast [<address>]]  [[-]pointopoint [<address>]]
  [netmask <address>]  [dstaddr <address>]  [tunnel <address>]
  [outfill <NN>] [keepalive <NN>]
  [hw <HW> <address>]  [mtu <NN>]
  [[-]trailers]  [[-]arp]  [[-]allmulti]
  [multicast]  [[-]promisc]
  [mem_start <NN>]  [io_addr <NN>]  [irq <NN>]  [media <type>]
  [txqueuelen <NN>]
  [[-]dynamic]
  [up|down] ...

```

### --help
```sh
  <HW>=Hardware Type.
  List of possible hardware types:
    loop (Local Loopback) slip (Serial Line IP) cslip (VJ Serial Line IP) 
    slip6 (6-bit Serial Line IP) cslip6 (VJ 6-bit Serial Line IP) adaptive (Adaptive Serial Line IP) 
    ash (Ash) ether (Ethernet) ax25 (AMPR AX.25) 
    netrom (AMPR NET/ROM) rose (AMPR ROSE) tunnel (IPIP Tunnel) 
    ppp (Point-to-Point Protocol) hdlc ((Cisco)-HDLC) lapb (LAPB) 
    arcnet (ARCnet) dlci (Frame Relay DLCI) frad (Frame Relay Access Device) 
    sit (IPv6-in-IPv4) fddi (Fiber Distributed Data Interface) hippi (HIPPI) 
    irda (IrLAP) x25 (generic X.25) infiniband (InfiniBand) 
    eui64 (Generic EUI-64) 
  <AF>=Address family. Default: inet
  List of possible address families:
    unix (UNIX Domain) inet (DARPA Internet) inet6 (IPv6) 
    ax25 (AMPR AX.25) netrom (AMPR NET/ROM) rose (AMPR ROSE) 
    ipx (Novell IPX) ddp (Appletalk DDP) ash (Ash) 
    x25 (CCITT X.25) 

```

***

## [[NETWORKING]]

***
