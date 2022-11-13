#  Command [[rmmod]] :

***

## About:

### - remove device driver 

***

## Use Cases:

### - use rmmod to remove usb driver 
```sh
[bohdan@fedora /]$ lsmod | grep usb
usb_storage            81920  2 uas
btusb                  65536  0
btrtl                  28672  1 btusb
btbcm                  20480  1 btusb
btintel                49152  1 btusb
btmtk                  16384  1 btusb
bluetooth             806912  36 btrtl,btmtk,btintel,btbcm,bnep,btusb,rfcomm
[bohdan@fedora /]$ rmmod usb_storage

```

### - use to 
```sh

```


## Keys:
```sh
Options:
	-f, --force       forces a module unload and may crash your
	                  machine. This requires Forced Module Removal
	                  option in your kernel. DANGEROUS
	-s, --syslog      print to syslog, not stderr
	-v, --verbose     enables more messages
	-V, --version     show version
	-h, --help        show this help

```

### --help
```sh
Usage:
	rmmod [options] modulename ...

```

***

## [[Devices]]

***
