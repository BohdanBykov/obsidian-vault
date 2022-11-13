#  Command [[udevadm test]] :

***

## About:

### - devadm  test is a tool of Udev, that can show you all possible device events 

***


## Use Cases:

### - use udevadm test with my ssd 
```sh
[bohdan@fedora ~]$ udevadm test /sys/block/nvme0n1
This program is for debugging only, it does not run any program
specified by a RUN key. It may show incorrect results, because
some values may be different, or not available at a simulation run.

Trying to open "/etc/systemd/hwdb/hwdb.bin"...
Trying to open "/etc/udev/hwdb.bin"...
=== trie on-disk ===
tool version:          250
file size:        12003938 bytes
header size             80 bytes
strings            2439322 bytes
nodes              9564536 bytes
Load module index
Failed to read $container of PID 1, ignoring: Permission denied
Found cgroup2 on /sys/fs/cgroup/, full unified hierarchy
Found container virtualization none.
Loaded timestamp for '/etc/systemd/network'.
Loaded timestamp for '/run/systemd/network'.
Parsed configuration file /usr/lib/systemd/network/99-default.link
Created link configuration context.
Loaded timestamp for '/etc/udev/rules.d'.
Reading rules file: /usr/lib/udev/rules.d/01-md-raid-creating.rules
Reading rules file: /usr/lib/udev/rules.d/10-dm.rules
Reading rules file: /usr/lib/udev/rules.d/11-dm-lvm.rules
...
```

### - use to 
```sh

```


## Keys:
```sh
Test an event run.

  -h --help                            Show this help
  -V --version                         Show package version
  -a --action=ACTION|help              Set action string
  -N --resolve-names=early|late|never  When to resolve names
```

### --help
```sh
[bohdan@fedora ~]$ udevadm test --help
udevadm test [OPTIONS] DEVPATH

```

***

## [[Devices]]

***
