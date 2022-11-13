#  Command [[tree]] :

***

## About:

### -  show you a directory in tree view

***


## Use Cases:

### - use to show directories
```sh
[bohdan@fedora testdirectory]$ tree 
.
├── a1
├── a2
├── a3
├── dirtest
│   ├── test
│   ├── testfile
│   └── test.txt
├── error.txt
├── folder.txt
├── --help
├── permissions.txt
├── ps2.txt
└── test.txt

1 directory, 12 files
[bohdan@fedora testdirectory]$ 

```

### - use tree -L 2 to show only 2 levels
```sh
[bohdan@fedora testdirectory]$ tree -L 2
.
├── dirtest
│   └── testfile
├── permissions.txt
├── ps2.txt
└── test.txt


```

### --help
```sh
[bohdan@fedora testdirectory]$ tree --help
usage: tree [-acdfghilnpqrstuvxACDFJQNSUX] [-L level [-R]] [-H  baseHREF]
	[-T title] [-o filename] [-P pattern] [-I pattern] [--gitignore]
	[--matchdirs] [--metafirst] [--ignore-case] [--nolinks] [--inodes]
	[--device] [--sort[=]<name>] [--dirsfirst] [--filesfirst]
	[--filelimit #] [--si] [--du] [--prune] [--charset X]
	[--timefmt[=]format] [--fromfile] [--noreport] [--version] [--help]
	[--] [directory ...]
  ------- Listing options -------
  -a            All files are listed.
  -d            List directories only.
  -l            Follow symbolic links like directories.
  -f            Print the full path prefix for each file.
  -x            Stay on current filesystem only.
  -L level      Descend only level directories deep.
  -R            Rerun tree when max dir level reached.
  -P pattern    List only those files that match the pattern given.
  -I pattern    Do not list files that match the given pattern.
  --gitignore   Filter by using .gitignore files.
  --ignore-case Ignore case when pattern matching.
  --matchdirs   Include directory names in -P pattern matching.
  --metafirst   Print meta-data at the beginning of each line.
  --info        Print information about files found in .info files.
  --noreport    Turn off file/directory count at end of tree listing.
  --charset X   Use charset X for terminal/HTML and indentation line output.
  --filelimit # Do not descend dirs with more than # files in them.
  -o filename   Output to file instead of stdout.
  --du          Print directory sizes.
  --prune       Prune empty directories from the output.
  ------- File options -------
  -q            Print non-printable characters as '?'.
  -N            Print non-printable characters as is.
  -Q            Quote filenames with double quotes.
  -p            Print the protections for each file.
  -u            Displays file owner or UID number.
  -g            Displays file group owner or GID number.
  -s            Print the size in bytes of each file.
  -h            Print the size in a more human readable way.
  --si          Like -h, but use in SI units (powers of 1000).
  -D            Print the date of last modification or (-c) status change.
  --timefmt <f> Print and format time according to the format <f>.
  -F            Appends '/', '=', '*', '@', '|' or '>' as per ls -F.
  --inodes      Print inode number of each file.
  --device      Print device ID number to which each file belongs.
  ------- Sorting options -------
  -v            Sort files alphanumerically by version.
  -t            Sort files by last modification time.
  -c            Sort files by last status change time.
  -U            Leave files unsorted.
  -r            Reverse the order of the sort.
  --dirsfirst   List directories before files (-U disables).
  --filesfirst  List files before directories (-U disables).
  --sort X      Select sort: name,version,size,mtime,ctime.
  ------- Graphics options -------
  -i            Don't print indentation lines.
  -A            Print ANSI lines graphic indentation lines.
  -S            Print with CP437 (console) graphics indentation lines.
  -n            Turn colorization off always (-C overrides).
  -C            Turn colorization on always.
  ------- XML/HTML/JSON options -------
  -X            Prints out an XML representation of the tree.
  -J            Prints out an JSON representation of the tree.
  -H baseHREF   Prints out HTML format with baseHREF as top directory.
  -T string     Replace the default HTML title and H1 header with string.
  --nolinks     Turn off hyperlinks in HTML output.
  ------- Input options -------
  --fromfile    Reads paths from files (.=stdin)
  ------- Miscellaneous options -------
  --version     Print version and exit.
  --help        Print usage and this help message and exit.
  --            Options processing terminator.

```

***

## [[FILES]] * [[USEFUL]]

***
