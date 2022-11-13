#  Command [[modinfo]] :

***

## About:

### - show info about kernel module

***

## Use Cases:

### - use modinfo to show info about ssd (from lsmod)
```sh
[bohdan@fedora ~]$ modinfo nvme
filename:       /lib/modules/5.19.12-200.fc36.x86_64/kernel/drivers/nvme/host/nvme.ko.xz
version:        1.0
license:        GPL
author:         Matthew Wilcox <willy@linux.intel.com>
srcversion:     E20D9341AC72133459FEBC1
alias:          pci:v*d*sv*sd*bc01sc08i02*
alias:          pci:v0000106Bd00002005sv*sd*bc*sc*i*
alias:          pci:v0000106Bd00002003sv*sd*bc*sc*i*
alias:          pci:v0000106Bd00002001sv*sd*bc*sc*i*
alias:          pci:v00001D0Fd0000CD02sv*sd*bc*sc*i*
alias:          pci:v00001D0Fd0000CD01sv*sd*bc*sc*i*

```

### - use to 
```sh

```


## Keys:
```sh
Options:
	-a, --author                Print only 'author'
	-d, --description           Print only 'description'
	-l, --license               Print only 'license'
	-p, --parameters            Print only 'parm'
	-n, --filename              Print only 'filename'
	-0, --null                  Use \0 instead of \n
	-F, --field=FIELD           Print only provided FIELD
	-k, --set-version=VERSION   Use VERSION instead of `uname -r`
	-b, --basedir=DIR           Use DIR as filesystem root for /lib/modules
	-V, --version               Show version
	-h, --help                  Show this help

```

### --help
```sh
Usage:
	modinfo [options] filename [args]

```

***

## [[Devices]]

***
