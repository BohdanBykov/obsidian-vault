#  Command [[clear]] :

***

## About:

### -  clear your cli

***


## Use Cases:

### - use to 
```sh
[bohdan@fedora testdirectory]$ ls
a1  a2  a3  permissions.txt  ps2.txt  testdir
[bohdan@fedora testdirectory]$ clear

[bohdan@fedora testdir]$
```


## Keys:
```sh
OPTIONS
       -T type
            indicates the type of terminal.  Normally this option is unnecessary, because the default is taken from the  environment  variable
            TERM.  If -T is specified, then the shell variables LINES and COLUMNS will also be ignored.

       -V   reports the version of ncurses which was used in this program, and exits.  The options are as follows:

       -x   do not attempt to clear the terminal's scrollback buffer using the extended “E3” capability.

```

### --help
```sh
SYNOPSIS
       clear [-Ttype] [-V] [-x]

DESCRIPTION
       clear  clears  your  screen  if  this is possible, including its scrollback buffer (if the extended “E3” capability is defined).  clear
       looks in the environment for the terminal type given by the environment variable TERM, and then in the terminfo database  to  determine
       how to clear the screen.

       clear  writes  to the standard output.  You can redirect the standard output to a file (which prevents clear from actually clearing the
       screen), and later cat the file to the screen, clearing it at that point.

```

***

## [[USEFUL]]

***
