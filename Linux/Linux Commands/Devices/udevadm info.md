#  Command [[udevadm info]]:

***

## About:

### - udevadm  info is a tool of Udev, that can show you device info from udev db

***


## Use Cases:

### - use udevadm info -a(attributes) -p(path)
```sh
[bohdan@fedora ~]$ ls /sys/class/net
docker0  enp3s0  lo  wlp4s0
[bohdan@fedora ~]$ udevadm info -a -p /sys/class/net/wlp4s0

Udevadm info starts with the device specified by the devpath and then
walks up the chain of parent devices. It prints for every device
found, all possible attributes in the udev rules key format.
A rule to match, can be composed by the attributes of the device
and the attributes from one single parent device.

  looking at device '/devices/pci0000:00/0000:00:02.1/0000:04:00.0/net/wlp4s0':
    KERNEL=="wlp4s0"
    SUBSYSTEM=="net"
    DRIVER==""
    ATTR{addr_assign_type}=="3"
    ATTR{addr_len}=="6"
    ATTR{address}=="94:08:53:89:06:a1"
    ATTR{broadcast}=="ff:ff:ff:ff:ff:ff"
    ATTR{carrier}=="1"
    ATTR{carrier_changes}=="4"
    ATTR{carrier_down_count}=="2"
    ATTR{carrier_up_count}=="2"
    ATTR{dev_id}=="0x0"
    ATTR{dev_port}=="0"
    ATTR{dormant}=="0"
    ATTR{flags}=="0x1003"
    ATTR{gro_flush_timeout}=="0"
    ATTR{ifalias}==""
    ATTR{ifindex}=="3"
    ATTR{iflink}=="3"
    ATTR{link_mode}=="1"
...
```

### - use udevadm info  
```sh

```

## Keys:
```sh
  -h --help                   Print this message
  -V --version                Print version of the program
  -q --query=TYPE             Query device information:
       name                     Name of device node
       symlink                  Pointing to node
       path                     sysfs device path
       property                 The device properties
       all                      All values
     --property=NAME          Show only properties by this name
     --value                  When showing properties, print only their values
  -p --path=SYSPATH           sysfs device path used for query or attribute walk
  -n --name=NAME              Node or symlink name used for query or attribute walk
  -r --root                   Prepend dev directory to path names
  -a --attribute-walk         Print all key matches walking along the chain
                              of parent devices
  -d --device-id-of-file=FILE Print major:minor of device containing this file
  -x --export                 Export key/value pairs
  -P --export-prefix          Export the key name with a prefix
  -e --export-db              Export the content of the udev database
  -c --cleanup-db             Clean up the udev database
  -w --wait-for-initialization[=SECONDS]
                              Wait for device to be initialized

```

### --help
```sh
[bohdan@fedora ~]$ udevadm info --help
udevadm info [OPTIONS] [DEVPATH|FILE]

```

***

## [[Devices]]

***
