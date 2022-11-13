#  Command [[chmod]] :

***

## About:

### - change permissions to file

***


## Use Cases:

### - use chmod with numbers to change [[PERMISSIONS]] of the file 
```sh
[bohdan@fedora testdirectory]$ ls -l
total 24
drwxr-xr-x. 1 bohdan bohdan    60 Oct 13 11:29 dirtest
-rwxr-----. 1 bohdan bohdan    48 Oct  8 20:29 permissions.txt
-rw-r--r--. 1 bohdan bohdan 14097 Oct  9 10:49 ps2.txt
-rw-r--r--. 1 bohdan bohdan    20 Oct 13 12:27 test.txt
[bohdan@fedora testdirectory]$ chmod 777 permissions.txt
[bohdan@fedora testdirectory]$ ls -l
total 24
drwxr-xr-x. 1 bohdan bohdan    60 Oct 13 11:29 dirtest
-rwxrwxrwx. 1 bohdan bohdan    48 Oct  8 20:29 permissions.txt
-rw-r--r--. 1 bohdan bohdan 14097 Oct  9 10:49 ps2.txt
-rw-r--r--. 1 bohdan bohdan    20 Oct 13 12:27 test.txt
[bohdan@fedora testdirectory]$ 
```

### - use chmod +/- to add [[PERMISSIONS]] 
```sh
[bohdan@fedora testdirectory]$ ls -l
total 24
-rw-rw-rw-. 1 bohdan bohdan    48 Oct  8 20:29 permissions.txt
[bohdan@fedora testdirectory]$ chmod +x permissions.txt
[bohdan@fedora testdirectory]$ ls -l
total 24
-rwxrwxrwx. 1 bohdan bohdan    48 Oct  8 20:29 permissions.txt
[bohdan@fedora testdirectory]$ 
```

### - use chmod g-x to change [[PERMISSIONS]] for the group 
```sh
[bohdan@fedora testdirectory]$ ls -l
total 24
drwxr-xr-x. 1 bohdan bohdan    60 Oct 13 11:29 dirtes
-rwxrwxrwx. 1 bohdan bohdan    48 Oct  8 20:29 permissions.txt
[bohdan@fedora testdirectory]$ chmod g-x permissions.txt
[bohdan@fedora testdirectory]$ ls -l
total 24
-rwxrw-rwx. 1 bohdan bohdan    48 Oct  8 20:29 permissions.txt
[bohdan@fedora testdirectory]$ 
```




## Keys:
```sh
  -c, --changes          like verbose but report only when a change is made
  -f, --silent, --quiet  suppress most error messages
  -v, --verbose          output a diagnostic for every file processed
      --no-preserve-root  do not treat '/' specially (the default)
      --preserve-root    fail to operate recursively on '/'
      --reference=RFILE  use RFILE's mode instead of MODE values
  -R, --recursive        change files and directories recursively

```

### --help
```sh
[bohdan@fedora testdirectory]$ chmod --help
Usage: chmod [OPTION]... MODE[,MODE]... FILE...
  or:  chmod [OPTION]... OCTAL-MODE FILE...
  or:  chmod [OPTION]... --reference=RFILE FILE...
Change the mode of each FILE to MODE.
With --reference, change the mode of each FILE to that of RFILE.

Each MODE is of the form '[ugoa]*([-+=]([rwxXst]*|[ugo]))+|[-+=][0-7]+'.

```

***

## [[PERMISSIONS]]

***
