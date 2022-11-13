#  Command [[kill]] :

***

## About:

### - stop your proccess immediatly

***

## Use Cases:

### - use kill pid to stop process 
```sh
[bohdan@fedora ~]$ ps aux | tail | grep telegram-desktop
bohdan     13529  0.0  0.0   3724  1400 ?        S    09:44   0:00 bwrap --args 41 telegram-desktop --
bohdan     13530 12.3  3.5 1375492 413272 ?      Sl   09:44   0:28 telegram-desktop --
bohdan     14170  0.0  0.0 222300  2188 pts/0    S+   09:48   0:00 grep --color=auto telegram-desktop
[bohdan@fedora ~]$ sudo kill 13530
[sudo] password for bohdan: 
[bohdan@fedora ~]$ ps aux | tail | grep telegram-desktop
bohdan     14332  0.0  0.0 222300  2256 pts/0    S+   09:49   0:00 grep --color=auto telegram-desktop
[bohdan@fedora ~]$ 

```

### - use to 
```sh

```


## Keys:
```sh
    Options:
      -s sig	SIG is a signal name
      -n sig	SIG is a signal number
      -l	list the signal names; if arguments follow `-l' they are
    		assumed to be signal numbers for which names should be listed
      -L	synonym for -l

```

### --help
```sh
kill: kill [-s sigspec | -n signum | -sigspec] pid | jobspec ... or kill -l [sigspec]
    Send a signal to a job.
    
    Send the processes identified by PID or JOBSPEC the signal named by
    SIGSPEC or SIGNUM.  If neither SIGSPEC nor SIGNUM is present, then
    SIGTERM is assumed.
    
   Kill is a shell builtin for two reasons: it allows job IDs to be used
    instead of process IDs, and allows processes to be killed if the limit
    on processes that you can create is reached.
    
    Exit Status:
    Returns success unless an invalid option is given or an error occurs.

```

***

## [[PROCESSES]]

***
