#  Command [[lsmod]] :

***

## About:

### - show the status of the modules in kernel core. It can be drivers or some funtions 

***

## Use Cases:

### - use lsmod 
```sh
[bohdan@fedora ~]$ lsmod
Module                  Size  Used by
tls                   118784  0
uinput                 20480  1
rfcomm                 90112  7
snd_seq_dummy          16384  0
snd_hrtimer            16384  1
xt_conntrack           16384  1
xt_MASQUERADE          20480  1
nf_conntrack_netlink    53248  0
xt_addrtype            16384  2
nft_compat             20480  4
br_netfilter           32768  0
bridge                352256  1 br_netfilter
stp                    16384  1 bridge
llc                    16384  2 bridge,stp
...
```

***

## [[Devices]]

***
