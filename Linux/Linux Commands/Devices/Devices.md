***

# sysfs, devfs, udev   (LPIC 101.1)

***

- ## HAL - Hardware Abstracture Level ( !Old)

	 This is subsystem for UNIX-like OS, that provide some abstract layer above hardware with what OS speaks.  

- ## Dbus - Desktop Bus

	 Dbus is mechanism that allows us get information about hardware from kernel core.

- ## Udev - userspace [[dev dir]]

	 Part of [[kernel-core]], that is a new generation of HAL, it organize all devices in [[dev dir]] directory.

	 Udev advantages:
	 - working on the user layer
	 - react on hardware changes (usb plug in etc.)
	 - provide human-readable configuration files
	 - store configs only of active devices
	 - save device names if they were reconnected
![[Pasted image 20221021145158.png]]


- ## Devfs - Device filesystem ( !Old)

	 This is virtual file system that working in ram and mount in [[dev dir]] dir.
	 Now all the files it contain create Udev:
	 - mem - image of physical memory
	 - null - empty device
	 - pts/ - pseudo-terminal (virtual tty)
	 - urandom - random numbers generator
	 - sdx - pluggable devices
	 - tty - teletype terminal (function to speak with computer)


- ## Sysfs - System filesystem (Udev part)
	 Also pseudo file system, provided by kernel that export information about drivers and devices on user layer. Mount in /sys
	- devices/ - all deviced registered in the core
	- bus/        - list of buses
	- drivers/   - list of drivers
	- block/     - catalog of block devices (pluggable devices)
	- class/      - class grupped devices
	![[Pasted image 20221021144840.png]]
- ## Procfs - Proc filesystem
	 Special filesystem that present information about processes and other system information in hierarhical file. Mount in /proc
	 - PID/        - info about some process
	 - cpuinfo/ - info about cpu
	 - devices/ - list of connected devices
	 - mounts/ - mounted file systems
	 - sys/        - system information you can redact
	
![[Pasted image 20221021145133.png]]
***

## [[Linux Commands]]