#  Command [[udevadm monitor]] :

***

## About:

### - udevadm  monitor is a tool of Udev, that can show you recent events with devices (plug/unplug)

***

## Use Cases:

### - use udevadm monitor events (plug in usb) 
```sh
[bohdan@fedora ~]$ udevadm  monitor --property --kernel
monitor will print the received events for:
KERNEL - the kernel uevent

KERNEL[7729.877443] add      /devices/pci0000:00/0000:00:08.1/0000:05:00.4/usb3/3-3 (usb)
ACTION=add
DEVPATH=/devices/pci0000:00/0000:00:08.1/0000:05:00.4/usb3/3-3
SUBSYSTEM=usb
DEVNAME=/dev/bus/usb/003/008
DEVTYPE=usb_device
PRODUCT=abcd/1234/100
TYPE=0/0/0
BUSNUM=003
DEVNUM=008
SEQNUM=4294
MAJOR=189
MINOR=263

```

### - use to 
```sh

```


## Keys:
```sh
Listen to kernel and udev events.

  -h --help                                Show this help
  -V --version                             Show package version
  -p --property                            Print the event properties
  -k --kernel                              Print kernel uevents
  -u --udev                                Print udev events
  -s --subsystem-match=SUBSYSTEM[/DEVTYPE] Filter events by subsystem
  -t --tag-match=TAG                       Filter events by tag
[bohdan@fedora ~]$ 


```

### --help
```sh
[bohdan@fedora ~]$ udevadm monitor --help
udevadm monitor [OPTIONS]
```

***

## [[Devices]]

***
