***

## Directory Udev use to contain devices.

***

- ### /dev/null
	 Directory that emulate empty device
	 You can use it as a wastebucket  

use > dev/null 2>&1 to send error in wastebucket
```sh 
[bohdan@fedora ~]$ noneprogram
bash: noneprogram: command not found...
Failed to search for file: Failed to load /etc/yum.repos.d/.repo: Invalid group name: 
[bohdan@fedora ~]$ noneprogram > /dev/null 2>&1
[bohdan@fedora ~]$ 
```

***

## [[Devices]]