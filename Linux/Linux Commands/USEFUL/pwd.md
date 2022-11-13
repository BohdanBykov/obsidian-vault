#  Command [[pwd]] :

***

## About:

### - show path to your directory

***


## Use Cases:

### - use to find where are you 
```sh
[bohdan@fedora testdirectory]$ pwd
/home/bohdan/testdirectory
[bohdan@fedora testdirectory]$ 
```


## Keys:
```sh
    Options:
      -L	print the value of $PWD if it names the current working
    		directory
      -P	print the physical directory, without any symbolic links

```

### --help
```sh
[bohdan@fedora testdirectory]$ pwd --help
pwd: pwd [-LP]
    Print the name of the current working directory.

    By default, `pwd' behaves as if `-L' were specified.
    
    Exit Status:
    Returns 0 unless an invalid option is given or the current directory
    cannot be read.

```

***

## [[FILES]]

***
