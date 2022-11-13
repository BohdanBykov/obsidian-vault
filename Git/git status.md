#  Command [[git status]] :

***

## About:

### - show changes in working directory

***

## Use Cases:

### - use to 
```sh
[bohdan@fedora gittest]$ git status
On branch master
nothing to commit, working tree clean
[bohdan@fedora gittest]$ touch testfile
[bohdan@fedora gittest]$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
	testfile

nothing added to commit but untracked files present (use "git add" to track)
[bohdan@fedora gittest]$ 
```

### - use to 
```sh

```


## Keys:
```sh
OPTIONS
       -s, --short
           Give the output in the short-format.

       -b, --branch
           Show the branch and tracking info even in short-format.

       --show-stash
           Show the number of entries currently stashed away.

       --porcelain[=<version>]
           Give the output in an easy-to-parse format for scripts. This is 
           similar to the short output, but will remain stable
           across Git versions and regardless of user configuration. See below 
           for details.
           The version parameter is used to specify the format version. This is 
           optional and defaults to the original version v1
           format.

       --long
           Give the output in the long-format. This is the default.

       -v, --verbose
           In addition to the names of files that have been changed, also show 
           the textual changes that are staged to be committed
           (i.e., like the output of git diff --cached). If -v is specified  
           twice, then also show the changes in the working tree
           that have not yet been staged (i.e., like the output of git diff).

       -u[<mode>], --untracked-files[=<mode>]
           Show untracked files.

           The mode parameter is used to specify the handling of untracked files. 
           It is optional: it defaults to all, and if
           specified, it must be stuck to the option (e.g.  -uno, but not -u no).
```

### --help
```sh
git status [<options>...] [--] [<pathspec>...]
```

***

