***
## About:
grep - (global regular expression print)
grep is a tool that can search for a specified pattern or patterns in a text file.
It copy each line of file in buffer and print it only if it match search pattern.

***
```sh
#a_file
boot 
book
booze
machine
boots
bungie
bark
aardvark
broken$tuff
robots
grep
grep grep
```

## Use Cases:
---
- #### search for "boo" string in a_file
```sh
╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ grep "boo" a_file
boot 
book
booze
boots
```

 ---
 - #### (-n) specify row number 
```sh
╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ grep -n "boo" a_file
1:boot 
2:book
3:booze
5:boots
```

---
 - #### (-v) print rows that don't match search pattern
```sh
╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ grep -vn "boo" a_file
4:machine
6:bungie
7:bark
8:aardvark
9:broken$tuff
10:robots
```

---
- #### (-c) print number of rows matched search pattern
```sh
╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ grep "boo" a_file    
boot 
book
booze
boots
--------------------------------------------------------------------------------- 
╰─$ grep -c "boo" a_file
4
```

---
- #### (-l) print name of files that include string you search
```sh
╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ grep -l "boo" *
a_file
```

---
- #### (-i) ignore (upper/lower) case
```sh
╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ grep -i "BOO" a_file
boot 
book
booze
boots
```

---
- #### (-x) search for exact matches in row only
```sh
╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ grep -nx "grep" a_file
11:grep
```

---
- #### (-A) additional rows to search result
```sh
╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ grep -A2 "mach" a_file
machine
boots
bungie
```

### [Regular Expressions](https://gnosis.cx/publish/programming/regular_expressions.html)

---
- #### ($) search with string in the end
```sh
╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ grep "e$" a_file
booze
machine
bungie
```

- #### (-E) use wider range of regexp commands
---
- #### (?) print results that match +- 1 letter before "?"
```sh
╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ grep -E "boots?" a_file                                                                                                                                             
boot 
boots
```

---
- #### ( \| ) combine search patterns in "or" statement
```sh
╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ grep -E "boots|machine" a_file
machine
boots
```

---
- #### ( \\ ) ignore special character
```sh
╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ grep '\$' a_file
broken$tuff
```

***
### Help:
```sh
Usage: grep [OPTION]... PATTERNS [FILE]...
```

***
### Keys:
```sh
Pattern selection and interpretation:
  -E, --extended-regexp     PATTERNS are extended regular expressions
  -F, --fixed-strings       PATTERNS are strings
  -G, --basic-regexp        PATTERNS are basic regular expressions
  -P, --perl-regexp         PATTERNS are Perl regular expressions
  -e, --regexp=PATTERNS     use PATTERNS for matching
  -f, --file=FILE           take PATTERNS from FILE
  -i, --ignore-case         ignore case distinctions in patterns and data
      --no-ignore-case      do not ignore case distinctions (default)
  -w, --word-regexp         match only whole words
  -x, --line-regexp         match only whole lines
  -z, --null-data           a data line ends in 0 byte, not newline

Miscellaneous:
  -s, --no-messages         suppress error messages
  -v, --invert-match        select non-matching lines
  -V, --version             display version information and exit
      --help                display this help text and exit

Output control:
  -m, --max-count=NUM       stop after NUM selected lines
  -b, --byte-offset         print the byte offset with output lines
  -n, --line-number         print line number with output lines
      --line-buffered       flush output on every line
  -H, --with-filename       print file name with output lines
  -h, --no-filename         suppress the file name prefix on output
      --label=LABEL         use LABEL as the standard input file name prefix
  -o, --only-matching       show only nonempty parts of lines that match
  -q, --quiet, --silent     suppress all normal output
      --binary-files=TYPE   assume that binary files are TYPE;
                            TYPE is 'binary', 'text', or 'without-match'
  -a, --text                equivalent to --binary-files=text
  -I                        equivalent to --binary-files=without-match
  -d, --directories=ACTION  how to handle directories;
                            ACTION is 'read', 'recurse', or 'skip'
  -D, --devices=ACTION      how to handle devices, FIFOs and sockets;
                            ACTION is 'read' or 'skip'
  -r, --recursive           like --directories=recurse
  -R, --dereference-recursive
                            likewise, but follow all symlinks
      --include=GLOB        search only files that match GLOB (a file pattern)
      --exclude=GLOB        skip files that match GLOB
      --exclude-from=FILE   skip files that match any file pattern from FILE
      --exclude-dir=GLOB    skip directories that match GLOB
  -L, --files-without-match print only names of FILEs with no selected lines
  -l, --files-with-matches  print only names of FILEs with selected lines
  -c, --count               print only a count of selected lines per FILE
  -T, --initial-tab         make tabs line up (if needed)
  -Z, --null                print 0 byte after FILE name

Context control:
  -B, --before-context=NUM  print NUM lines of leading context
  -A, --after-context=NUM   print NUM lines of trailing context
  -C, --context=NUM         print NUM lines of output context
  -NUM                      same as --context=NUM
      --group-separator=SEP  print SEP on line between matches with context
      --no-group-separator  do not print separator for matches with context
      --color[=WHEN],
      --colour[=WHEN]       use markers to highlight the matching strings;
                            WHEN is 'always', 'never', or 'auto'
  -U, --binary              do not strip CR characters at EOL (MSDOS/Windows)

```
***
