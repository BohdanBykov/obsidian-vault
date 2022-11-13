#  Command [[rmdir]] :

***

## About:

### -  remove directories

***


## Use Cases:

### - use rmdir to remove empty directory
```sh
[bohdan@fedora testdirectory]$ ls
permissions.txt  ps2.txt  testdir  testdir2  testdir3  test.txt
[bohdan@fedora testdirectory]$ rmdir testdir3
[bohdan@fedora testdirectory]$ ls
permissions.txt  ps2.txt  testdir  testdir2  test.txt
[bohdan@fedora testdirectory]$ 
```


## Keys:
```sh
      --ignore-fail-on-non-empty
                  ignore each failure that is solely because a directory
                    is non-empty
  -p, --parents   remove DIRECTORY and its ancestors; e.g., 'rmdir -p a/b/c' is
                    similar to 'rmdir a/b/c a/b a'
  -v, --verbose   output a diagnostic for every directory processed

```

### --help
```sh
[bohdan@fedora testdirectory]$ rmdir --help
Usage: rmdir [OPTION]... DIRECTORY...
Remove the DIRECTORY(ies), if they are empty.
```

***

## [[FILES]]

***
