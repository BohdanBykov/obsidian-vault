#  Command [[rm]] :

***

## About:

### -  remove files or folders

***


## Use Cases:

### - use rm to delete file
```sh
[bohdan@fedora testdirectory]$ ls
permissions.txt  ps2.txt  testdir  testdir2  test.txt
[bohdan@fedora testdirectory]$ rm test.txt
[bohdan@fedora testdirectory]$ ls
permissions.txt  ps2.txt  testdir  testdir2
[bohdan@fedora testdirectory]$ 
```

### - use rm -i to delete couple of files
```sh
[bohdan@fedora testdirectory]$ ls
a1  a2  a3  dirtest  permissions.txt  ps2.txt  test.txt
[bohdan@fedora testdirectory]$ rm -i a1 a2 a3
rm: remove regular empty file 'a1'? y
rm: remove regular empty file 'a2'? y
rm: remove regular empty file 'a3'? y
[bohdan@fedora testdirectory]$ ls
dirtest  permissions.txt  ps2.txt  test.txt
[bohdan@fedora testdirectory]$ 

```

### - use rm -rf to remove files/directories without exceptions
```sh
[bohdan@fedora testdirectory]$ ls testdir2
test
[bohdan@fedora testdirectory]$ rm -rf testdir2
[bohdan@fedora testdirectory]$ ls
permissions.txt  ps2.txt  testdir
[bohdan@fedora testdirectory]$ 
```

### - use rm -- to delete file starts with -
```sh
[bohdan@fedora testdirectory]$ ls
a1  a2  a3  dirtest  folder.txt  --help  permissions.txt  ps2.txt  test.txt
[bohdan@fedora testdirectory]$ rm -- --help
[bohdan@fedora testdirectory]$ ls
a1  a2  a3  dirtest  folder.txt  permissions.txt  ps2.txt  test.txt
[bohdan@fedora testdirectory]$ 

```


## Keys:
```sh
  -f, --force           ignore nonexistent files and arguments, never prompt
  -i                    prompt before every removal
  -I                    prompt once before removing more than three files, or
                          when removing recursively; less intrusive than -i,
                          while still giving protection against most mistakes
      --interactive[=WHEN]  prompt according to WHEN: never, once (-I), or
                          always (-i); without WHEN, prompt always
      --one-file-system  when removing a hierarchy recursively, skip any
                          directory that is on a file system different from
                          that of the corresponding command line argument
      --no-preserve-root  do not treat '/' specially
      --preserve-root[=all]  do not remove '/' (default);
                              with 'all', reject any command line argument
                              on a separate device from its parent
  -r, -R, --recursive   remove directories and their contents recursively
  -d, --dir             remove empty directories

```

### --help
```sh
[bohdan@fedora testdirectory]$ rm --help
Usage: rm [OPTION]... [FILE]...
Remove (unlink) the FILE(s).

By default, rm does not remove directories.  Use the --recursive (-r or -R)
option to remove each listed directory, too, along with all of its contents.

To remove a file whose name starts with a '-', for example '-foo',
use one of these commands:
  rm -- -foo

  rm ./-foo

Note that if you use rm to remove a file, it might be possible to recover
some of its contents, given sufficient expertise and/or time.  For greater
assurance that the contents are truly unrecoverable, consider using shred(1).

```

***

## [[FILES]]

***
