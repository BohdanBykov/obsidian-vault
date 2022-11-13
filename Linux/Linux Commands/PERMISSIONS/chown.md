#  Command [[chown]] :

***

## About:

### - can change owner of the file

***


## Use Cases:

### - use chown user:group to change owner of the file 
```sh
[bohdan@fedora dirtest]$ ls -l
total 0
-rw-r--r--. 1 bohdan bohdan 0 Oct 11 15:50 testfile
[bohdan@fedora dirtest]$ sudo chown test:bohdan testfile
[sudo] password for bohdan:  
[bohdan@fedora dirtest]$ ls -l
total 0
-rw-r--r--. 1 test bohdan 0 Oct 11 15:50 testfile
[bohdan@fedora dirtest]$ 

```

### - use chown root  to change file owner to root 
```sh
[bohdan@fedora dirtest]$ sudo chown root testfile
[bohdan@fedora dirtest]$ ls -l
total 0
-rw-r--r--. 1 root bohdan 0 Oct 11 15:50 testfile
[bohdan@fedora dirtest]$ 
```


## Keys:
```sh
  -c, --changes          like verbose but report only when a change is made
  -f, --silent, --quiet  suppress most error messages
  -v, --verbose          output a diagnostic for every file processed
      --dereference      affect the referent of each symbolic link (this is
                         the default), rather than the symbolic link itself
  -h, --no-dereference   affect symbolic links instead of any referenced file
                         (useful only on systems that can change the
                         ownership of a symlink)
      --from=CURRENT_OWNER:CURRENT_GROUP
                         change the owner and/or group of each file only if
                         its current owner and/or group match those specified
                         here.  Either may be omitted, in which case a match
                         is not required for the omitted attribute
      --no-preserve-root  do not treat '/' specially (the default)
      --preserve-root    fail to operate recursively on '/'
      --reference=RFILE  use RFILE's owner and group rather than
                         specifying OWNER:GROUP values
  -R, --recursive        operate on files and directories recursively

The following options modify how a hierarchy is traversed when the -R
option is also specified.  If more than one is specified, only the final
one takes effect.

  -H                     if a command line argument is a symbolic link
                         to a directory, traverse it
  -L                     traverse every symbolic link to a directory
                         encountered
  -P                     do not traverse any symbolic links (default)

```

### --help
```sh
[bohdan@fedora dirtest]$ chown --help
Usage: chown [OPTION]... [OWNER][:[GROUP]] FILE...
  or:  chown [OPTION]... --reference=RFILE FILE...
Change the owner and/or group of each FILE to OWNER and/or GROUP.
With --reference, change the owner and group of each FILE to those of RFILE.

Owner is unchanged if missing.  Group is unchanged if missing, but changed
to login group if implied by a ':' following a symbolic OWNER.
OWNER and GROUP may be numeric as well as symbolic.

Examples:
  chown root /u        Change the owner of /u to "root".
  chown root:staff /u  Likewise, but also change its group to "staff".
  chown -hR root /u    Change the owner of /u and subfiles to "root".

```

***

## [[PERMISSIONS]]

***
