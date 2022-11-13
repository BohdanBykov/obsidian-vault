#  Command [[touch]] :

***

## About:

### -  create files

***


## Use Cases:

### - use touch to create empty file
```sh
[bohdan@fedora testdirectory]$ ls
a1  a2  a3  permissions.txt  ps2.txt  testdir
[bohdan@fedora testdirectory]$ touch test
[bohdan@fedora testdirectory]$ ls
a1  a2  a3  permissions.txt  ps2.txt  test  testdir
[bohdan@fedora testdirectory]$ 
```

## Keys:
```sh
Mandatory arguments to long options are mandatory for short options too.
  -a                     change only the access time
  -c, --no-create        do not create any files
  -d, --date=STRING      parse STRING and use it instead of current time
  -f                     (ignored)
  -h, --no-dereference   affect each symbolic link instead of any referenced
                         file (useful only on systems that can change the
                         timestamps of a symlink)
  -m                     change only the modification time
  -r, --reference=FILE   use this file's times instead of current time
  -t STAMP               use [[CC]YY]MMDDhhmm[.ss] instead of current time
      --time=WORD        change the specified time:
                           WORD is access, atime, or use: equivalent to -a
                           WORD is modify or mtime: equivalent to -m

```

### --help
```sh
[bohdan@fedora testdirectory]$ touch --help
Usage: touch [OPTION]... FILE...
Update the access and modification times of each FILE to the current time.

A FILE argument that does not exist is created empty, unless -c or -h
is supplied.

A FILE argument string of - is handled specially and causes touch to
change the times of the file associated with standard output.

Note that the -d and -t options accept different time-date formats.

```

***

## [[TEXT]] * [[FILES]]

***
