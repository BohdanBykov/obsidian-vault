#  Command [[cd]] :
***

## About:

### - this is basic linux command used to go throw your directories

***


## Use Cases:

### - use to go throw directories
```sh
[bohdan@fedora testdirectory]$ ls
permissions.txt  ps2.txt  testdir  test.txt
[bohdan@fedora testdirectory]$ cd testdir
[bohdan@fedora testdir]$ 
```

### - use to go on directory up
```sh
[bohdan@fedora testdirectory]$ cd testdir
[bohdan@fedora testdir]$ cd ..
[bohdan@fedora testdirectory]$ 
```

### - use to go home
```sh
[bohdan@fedora testdirectory]$ cd ~
[bohdan@fedora ~]$ 
```

### - use to go one command back
```sh
[bohdan@fedora ~]$ cd testdirectory
[bohdan@fedora testdirectory]$ cd -
/home/bohdan
[bohdan@fedora ~]$
```

## Keys:
```
    Options:
      -L	force symbolic links to be followed: resolve symbolic
    		links in DIR after processing instances of `..'
      -P	use the physical directory structure without following
    		symbolic links: resolve symbolic links in DIR before
    		processing instances of `..'
      -e	if the -P option is supplied, and the current working
    		directory cannot be determined successfully, exit with
    		a non-zero status
      -@	on systems that support it, present a file with extended
    		attributes as a directory containing the file attributes
  
```

### --help
```
[bohdan@fedora ~]$ cd --help
cd: cd [-L|[-P [-e]] [-@]] [dir]
    Change the shell working directory.
    
    Change the current directory to DIR.  The default DIR is the value of the
    HOME shell variable.
    
    The variable CDPATH defines the search path for the directory containing
    DIR.  Alternative directory names in CDPATH are separated by a colon (:).
    A null directory name is the same as the current directory.  If DIR begins
    with a slash (/), then CDPATH is not used.
    
    If the directory is not found, and the shell option `cdable_vars' is set,
    the word is assumed to be  a variable name.  If that variable has a value,
    its value is used for DIR.
    
    Options:
      -L	force symbolic links to be followed: resolve symbolic
    		links in DIR after processing instances of `..'
      -P	use the physical directory structure without following
    		symbolic links: resolve symbolic links in DIR before
    		processing instances of `..'
      -e	if the -P option is supplied, and the current working
    		directory cannot be determined successfully, exit with
    		a non-zero status
      -@	on systems that support it, present a file with extended
    		attributes as a directory containing the file attributes
    
    The default is to follow symbolic links, as if `-L' were specified.
    `..' is processed by removing the immediately previous pathname component
    back to a slash or the beginning of DIR.
    
    Exit Status:
    Returns 0 if the directory is changed, and if $PWD is set successfully when
    -P is used; non-zero otherwise.
[bohdan@fedora ~]$ 

```


***

## [[FILES]] 

***
