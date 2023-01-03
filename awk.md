***
### About:
AWK is kind of pattern oriented language, using awk tool you can operate columns on each row of the file. You can use loops (for/while) or branching (if).
AWK statement include:
BEGIN { ... initialize awk commands (variables at exmp)}
{ awk commands that will operate each line of the file}
END { finalize commands (print output)}

***
## Use Cases:

- #### sum data from column
	- $5 means column 5, $0 means whole row 
```sh
╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ ls -l
total 104
-rw-r--r--. 1 bohdan bohdan     88 Jan  1 17:44 a_file
-rw-r--r--. 1 bohdan bohdan 101517 Jan  1 17:07 grep_awk_sed.pdf
-rw-r--r--. 1 bohdan bohdan      0 Jan  1 19:42 vi

---------------------------------------------------------------------------------╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ ls -l |awk 'BEGIN {sum=0} {sum=sum+$5} END {print sum}'                                                                                                            
101605
```

---
 - #### print every 3rd line (and the last one) with line numbers
	 - NR - row number, NF number of fields in line
```sh
╭─bohdan@fedora ~/github/for-tests/grep_awk_sed ‹main●› 
╰─$ ls -l|awk '{for (i=1;i<3;i++) {getline}; print NR, $0}'
3 -rw-r--r--. 1 bohdan bohdan 101517 Jan  1 17:07 grep_awk_sed.pdf
4 -rw-r--r--. 1 bohdan bohdan      0 Jan  1 19:42 vi
```

---
 - #### use to 
```sh

```

---
 - #### use to 
```sh

```

***
## AWK Pattern Matching:

AWK is a line-oriented language. The pattern comes first, and then the action. Action statements are enclosed in { and }. Either the pattern may be missing, or the action may be missing, but, of course, not both. If the pattern is missing, the action is executed for every single record of input. A missing action prints the entire record.

AWK patterns include regular expressions (uses same syntax as 'grep -E') and combinations using the special symbols '&&' means 'logical AND', '||' means 'logical OR', '!' means 'logical NOT'. You can also do relational patterns, groups of patterns, ranges, etc.

***
## AWK Control Statements:

| | | |
|-|-|
|if (condition) statement \[ else statement \]| |
|while (condition) statement| |
|do statement while (condition)| |
|for (expr1; expr2; expr3) statement| |
|for (var in array) statement| |
|break| |
|continue| |
|exit \[ expression \]| |

***
## AWK input/output statements include:
| | | |
|------------ | ------------| 
|close(file [, how]) |Close file, pipe or co-process. | 
|getline |Set $0 from next input record. | 
|getline <file |Set $0 from next record of file. | 
|getline var |Set var from next input record. | 
|getline var <file |Set var from next record of file. | 
|next |Stop processing the current input record. | 
|nextfile |Stop processing the current input record. |
|print |Prints the current record. |
|print expr-list|Prints expressions |
|print expr-list>file |Prints expressions on file. |
|printf fmt, expr-list |Format and print. | 

***
## AWK Numeric functions include:

| | |
|-|-|
|atan2(y, x) |Returns the arctangent of y/x in radians.|
|cos(expr)|Returns the cosine of expr, which is in radians.|
|exp(expr)|The exponential function.|
|int(expr)|Truncates to integer.|
|log(expr)|The natural logarithm function.|
|Rand()|Returns a random number N, between 0 and 1, such that 0 <= N < 1.|
|sin(expr)|Returns the sine of expr, which is in radians.|
|sqrt(expr)|The square root function.|
|srand([expr])| Uses expr as a new seed for the random number generator. If no expr is
| |provided, the time of day is used.|
***
## Help:
```sh

```

***
