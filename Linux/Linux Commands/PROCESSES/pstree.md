#  Command [[pstree]] :

***

## About:

### - show active processes in tree view

***


## Use Cases:

### - use pstree
```sh
[bohdan@fedora /]$ pstree
systemd─┬─ModemManager───3*[{ModemManager}]
        ├─NetworkManager───2*[{NetworkManager}]
        ├─abrt-dbus───2*[{abrt-dbus}]
        ├─3*[abrt-dump-journ]
        ├─abrtd───2*[{abrtd}]
        ├─accounts-daemon───3*[{accounts-daemon}]
        ├─alsactl
        ├─auditd───{auditd}
        ├─avahi-daemon───avahi-daemon
        ├─bluetoothd
        ├─chronyd
        ├─colord───3*[{colord}]
        ├─containerd───10*[{containerd}]
        ├─crond
        ├─cupsd
        ├─dbus-broker-lau───dbus-broker
        ├─dockerd───10*[{dockerd}]
        ├─firewalld───{firewalld}
        ├─gdm─┬─gdm-session-wor─┬─gdm-wayland-ses─┬─gnome-session-b───3*[{gnome-session-b}]
        │     │                 │                 └─2*[{gdm-wayland-ses}]
        │     │                 └─2*[{gdm-session-wor}]

```

### - use to 
```sh

```


## Keys:
```sh
Display a tree of processes.

  -a, --arguments     show command line arguments
  -A, --ascii         use ASCII line drawing characters
  -c, --compact-not   don't compact identical subtrees
  -C, --color=TYPE    color process by attribute
                      (age)
  -g, --show-pgids    show process group ids; implies -c
  -G, --vt100         use VT100 line drawing characters
  -h, --highlight-all highlight current process and its ancestors
  -H PID, --highlight-pid=PID
                      highlight this process and its ancestors
  -l, --long          don't truncate long lines
  -n, --numeric-sort  sort output by PID
  -N TYPE, --ns-sort=TYPE
                      sort output by this namespace type
                              (cgroup, ipc, mnt, net, pid, time, user, uts)
  -p, --show-pids     show PIDs; implies -c
  -s, --show-parents  show parents of the selected process
  -S, --ns-changes    show namespace transitions
  -t, --thread-names  show full thread names
  -T, --hide-threads  hide threads, show only processes
  -u, --uid-changes   show uid transitions
  -U, --unicode       use UTF-8 (Unicode) line drawing characters
  -V, --version       display version information
  -Z, --security-context
                      show security attributes

```

### --help
```sh
[bohdan@fedora /]$ pstree --help
pstree: unrecognized option '--help'
Usage: pstree [-acglpsStTuZ] [ -h | -H PID ] [ -n | -N type ]
              [ -A | -G | -U ] [ PID | USER ]
   or: pstree -V
   
  PID    start at this PID; default is 1 (init)
  USER   show only trees rooted at processes of this user
```

***

## [[PROCESSES]]

***
