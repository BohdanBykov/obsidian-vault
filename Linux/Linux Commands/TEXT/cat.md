#  Command [[cat]] :

***

## About:

### -  show file content

***

## Use Cases:

### - use cat to read file 
```sh
[bohdan@fedora testdirectory]$ cat test.txt
hello world
[bohdan@fedora testdirectory]$ 

```

### - use cat [[>]] to create text file
```sh
[bohdan@fedora testdirectory]$ cat > test.txt
hello world
^C
[bohdan@fedora testdirectory]$ 
```

### - use 'cat [[I]] [[cut]] -d: -f2' to show 2 column in text file
```sh
[bohdan@fedora testdirectory]$ cat > test.txt
1:one
2:two
3:three
^C
[bohdan@fedora testdirectory]$ cat test.txt | cut -d: -f2
one
two
three
[bohdan@fedora testdirectory]$
```



## Keys:
```sh
  -A, --show-all           equivalent to -vET
  -b, --number-nonblank    number nonempty output lines, overrides -n
  -e                       equivalent to -vE
  -E, --show-ends          display $ at end of each line
  -n, --number             number all output lines
  -s, --squeeze-blank      suppress repeated empty output lines
  -t                       equivalent to -vT
  -T, --show-tabs          display TAB characters as ^I
  -u                       (ignored)
  -v, --show-nonprinting   use ^ and M- notation, except for LFD and TAB

```

### --help
```sh
[bohdan@fedora testdirectory]$ cat --help
Usage: cat [OPTION]... [FILE]...
Concatenate FILE(s) to standard output.

With no FILE, or when FILE is -, read standard input.

Examples:
  cat f - g  Output f's contents, then standard input, then g's contents.
  cat        Copy standard input to standard output.

```

***

## [[TEXT]] * [[FILES]]

***
