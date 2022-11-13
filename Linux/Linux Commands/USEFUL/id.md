#  Command [[id]] :

***

## About:

### - show id of the user

***


## Use Cases:

### - use id to show current user id
```sh
[bohdan@fedora dirtest]$ id
uid=1000(bohdan) gid=1000(bohdan) groups=1000(bohdan),10(wheel) context=unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023
```

### - use id user to show users id 
```sh
[bohdan@fedora dirtest]$ id test
uid=1001(test) gid=1001(test) groups=1001(test)
```


## Keys:
```sh
  -a             ignore, for compatibility with other versions
  -Z, --context  print only the security context of the process
  -g, --group    print only the effective group ID
  -G, --groups   print all group IDs
  -n, --name     print a name instead of a number, for -ugG
  -r, --real     print the real ID instead of the effective ID, with -ugG
  -u, --user     print only the effective user ID
  -z, --zero     delimit entries with NUL characters, not whitespace;
                   not permitted in default format

```

### --help
```sh
[bohdan@fedora dirtest]$ id --help
Usage: id [OPTION]... [USER]...
Print user and group information for each specified USER,
or (when USER omitted) for the current user.

Without any OPTION, print some useful set of identified information.

```

***

## [[USEFUL]] * [[PERMISSIONS]]

***
