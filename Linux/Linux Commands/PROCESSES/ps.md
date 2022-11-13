#  Command [[ps]] :

***

## About:

### -  displays information about a selection of the active processes

***


## Use Cases:

### - use ps to show your active processes
```sh
[bohdan@fedora ~]$ ps
    PID TTY          TIME CMD
  18755 pts/0    00:00:00 bash
  39911 pts/0    00:00:00 ps
[bohdan@fedora ~]$ 

```

### - use ps aux to show all processes
```sh
[bohdan@fedora ~]$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.1 173496 18060 ?        Ss   09:22   0:02 /usr/lib/systemd/systemd rhgb --switched-root --system --deserialize 35
root           2  0.0  0.0      0     0 ?        S    09:22   0:00 [kthreadd]
root           3  0.0  0.0      0     0 ?        I<   09:22   0:00 [rcu_gp]
root           4  0.0  0.0      0     0 ?        I<   09:22   0:00 [rcu_par_gp]
root           5  0.0  0.0      0     0 ?        I<   09:22   0:00 [slub_flushwq]
root           6  0.0  0.0      0     0 ?        I<   09:22   0:00 [netns]
root           8  0.0  0.0      0     0 ?        I<   09:22   0:00 [kworker/0:0H-events_highpri]
root          10  0.0  0.0      0     0 ?        I<   09:22   0:00 [kworker/0:1H-events_highpri]
root          11  0.0  0.0      0     0 ?        I<   09:22   0:00 [mm_percpu_wq]
root          12  0.0  0.0      0     0 ?        I    09:22   0:11 [kworker/u32:1-btrfs-endio-write]
root          13  0.0  0.0      0     0 ?        I    09:22   0:00 [rcu_tasks_kthread]
root          14  0.0  0.0      0     0 ?        I    09:22   0:00 [rcu_tasks_rude_kthread]
...
```

### - use ps aux [[ I ]] [[less]] to show all processes in less
```sh
[bohdan@fedora ~]$ ps aux | less
```

![[Pasted image 20221012141150.png]]

## Keys:
```sh
EXAMPLES
       To see every process on the system using standard syntax:
          ps -e
          ps -ef
          ps -eF
          ps -ely

       To see every process on the system using BSD syntax:
          ps ax
          ps axu

       To print a process tree:
          ps -ejH
          ps axjf

       To get info about threads:
          ps -eLf
          ps axms

       To get security info:
          ps -eo euser,ruser,suser,fuser,f,comm,label
          ps axZ
          ps -eM

       To see every process running as root (real & effective ID) in user format:
          ps -U root -u root u

       To see every process with a user-defined format:
          ps -eo pid,tid,class,rtprio,ni,pri,psr,pcpu,stat,wchan:14,comm
          ps axo stat,euid,ruid,tty,tpgid,sess,pgrp,ppid,pid,pcpu,comm
          ps -Ao pid,tt,user,fname,tmout,f,wchan

       Print only the process IDs of syslogd:
          ps -C syslogd -o pid=

       Print only the name of PID 42:
          ps -q 42 -o comm=

```

### --help
```sh
NAME
       ps - report a snapshot of the current processes.

SYNOPSIS
       ps [options]

DESCRIPTION
       ps displays information about a selection of the active processes.  If you want a repetitive update of the selection and the displayed
       information, use top instead.

```

***

## [[PROCESSES]]

***
