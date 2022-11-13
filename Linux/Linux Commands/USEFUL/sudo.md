#  Command [[sudo]] :

***

## About:

### - launch command with as a root

***


## Use Cases:

### - use [[sudo]] -i to become root 
```sh
[bohdan@fedora testdirectory]$ sudo -i
[root@fedora ~]# 

```

### - use sudo [[tail]] /etc/passwd to show last 10 accounst 
```sh
[root@fedora ~]# sudo tail /etc/passwd
gdm:x:42:42:GNOME Display Manager:/var/lib/gdm:/sbin/nologin
gnome-initial-setup:x:985:982::/run/gnome-initial-setup/:/sbin/nologin
vboxadd:x:984:1::/var/run/vboxadd:/sbin/nologin
sshd:x:74:74:Privilege-separated SSH:/usr/share/empty.sshd:/sbin/nologin
tcpdump:x:72:72::/:/sbin/nologin
bohdan:x:1000:1000:bohdan:/home/bohdan:/bin/bash
systemd-coredump:x:978:978:systemd Core Dumper:/:/usr/sbin/nologin
systemd-timesync:x:977:977:systemd Time Synchronization:/:/usr/sbin/nologin
jenkins:x:976:975:Jenkins Automation Server:/var/lib/jenkins:/bin/false
mysql:x:27:27:MySQL Server:/var/lib/mysql:/sbin/nologin
[root@fedora ~]# 
```


## Keys:
```sh

Options:
  -A, --askpass                 use a helper program for password prompting
  -b, --background              run command in the background
  -B, --bell                    ring bell when prompting
  -C, --close-from=num          close all file descriptors >= num
  -D, --chdir=directory         change the working directory before running command
  -E, --preserve-env            preserve user environment when running command
      --preserve-env=list       preserve specific environment variables
  -e, --edit                    edit files instead of running a command
  -g, --group=group             run command as the specified group name or ID
  -H, --set-home                set HOME variable to target user's home dir
  -h, --help                    display help message and exit
  -h, --host=host               run command on host (if supported by plugin)
  -i, --login                   run login shell as the target user; a command may also be specified
  -K, --remove-timestamp        remove timestamp file completely
  -k, --reset-timestamp         invalidate timestamp file
  -l, --list                    list user's privileges or check a specific command; use twice for longer format
  -n, --non-interactive         non-interactive mode, no prompts are used
  -P, --preserve-groups         preserve group vector instead of setting to target's
  -p, --prompt=prompt           use the specified password prompt
  -R, --chroot=directory        change the root directory before running command
  -r, --role=role               create SELinux security context with specified role
  -S, --stdin                   read password from standard input
  -s, --shell                   run shell as the target user; a command may also be specified
  -t, --type=type               create SELinux security context with specified type
  -T, --command-timeout=timeout terminate command after the specified time limit
  -U, --other-user=user         in list mode, display privileges for user
  -u, --user=user               run command (or edit file) as specified user name or ID
  -V, --version                 display version information and exit
  -v, --validate                update user's timestamp without running a command
  --                            stop processing command line arguments

```

### --help
```sh
[root@fedora ~]# sudo --help
sudo - execute a command as another user

usage: sudo -h | -K | -k | -V
usage: sudo -v [-ABknS] [-g group] [-h host] [-p prompt] [-u user]
usage: sudo -l [-ABknS] [-g group] [-h host] [-p prompt] [-U user] [-u user] [command]
usage: sudo [-ABbEHknPS] [-r role] [-t type] [-C num] [-D directory] [-g group] [-h host] [-p prompt] [-R directory] [-T timeout] [-u user]
            [VAR=value] [-i|-s] [<command>]
usage: sudo -e [-ABknS] [-r role] [-t type] [-C num] [-D directory] [-g group] [-h host] [-p prompt] [-R directory] [-T timeout] [-u user] file
            ...

```

***

## [[PERMISSIONS]] * [[USEFUL]]

***
