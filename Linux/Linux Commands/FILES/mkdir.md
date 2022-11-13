#  Command [[mkdir]] :

***

## About:

### - can create a directory

***


## Use Cases:

### - use  mkdir to create directory
```sh
[bohdan@fedora testdirectory]$ ls
permissions.txt  ps2.txt  testdir  test.txt
[bohdan@fedora testdirectory]$ mkdir testdir2
[bohdan@fedora testdirectory]$ ls
permissions.txt  ps2.txt  testdir  testdir2  test.txt
[bohdan@fedora testdirectory]$ 
```

### - use  mkdir -m to create dir with  [[PERMISSIONS]]
```sh
[bohdan@fedora testdirectory]$ mkdir -m 740 testdir3
[bohdan@fedora testdirectory]$ ls -l
total 24
-rwxr-----. 1 bohdan bohdan    48 Oct  8 20:29 permissions.txt
-rw-r--r--. 1 bohdan bohdan 14097 Oct  9 10:49 ps2.txt
drwxr-xr-x. 1 bohdan bohdan    16 Oct  8 16:56 testdir
drwxr-xr-x. 1 bohdan bohdan     0 Oct 11 15:44 testdir2
drwxr-----. 1 bohdan bohdan     0 Oct 11 15:44 testdir3
-rw-r--r--. 1 bohdan bohdan    28 Oct  8 19:18 test.txt
[bohdan@fedora testdirectory]$ 

```


## Keys:
```
  -m, --mode=MODE   set file mode (as in chmod), not a=rwx - umask
  -p, --parents     no error if existing, make parent directories as needed,
                    with their file modes unaffected by any -m option.
  -v, --verbose     print a message for each created directory
  -Z                   set SELinux security context of each created directory
                         to the default type
      --context[=CTX]  like -Z, or if CTX is specified then set the SELinux
                         or SMACK security context to CTX

```

### --help
```
[bohdan@fedora testdirectory]$ mkdir --help
Usage: mkdir [OPTION]... DIRECTORY...
Create the DIRECTORY(ies), if they do not already exist.
```

***

## [[FILES]]

***
