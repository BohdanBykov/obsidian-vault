#  Operator [[I]] :

***

## About:

### - use output of first program as input to second program

***

## Use Cases:

### - use [[top]] I [[Linux/Linux Commands/USEFUL/grep]] to find my processes
```sh
[bohdan@fedora ~]$ top | grep bohdan
   2427 bohdan    20   0  528548  12372   6636 S   6.2   0.1   0:23.49 ibus-daemon                                                                
  42105 bohdan    20   0  848928  60744  50340 S   6.2   0.5   0:00.50 gnome-term                                                       
  42175 bohdan    20   0  226600   4324   3424 R   6.2   0.0   0:00.03 top                                                                        
  13416 bohdan    20   0 3569252 263980 148092 S   6.0   2.3   8:49.17 spotify                                                                    
   2177 bohdan    20   0 5980072 365228 173684 S   4.6   3.1  26:30.65 gnome-shell                                                                
  13499 bohdan    20   0   29.6g 432560 106132 S   3.0   3.7   9:04.39 spotify                                                                    
   2149 bohdan     9 -11  491304  19096  13608 S   1.7   0.2   1:47.42 wireplumber                                                                
   2305 bohdan     9 -11  288928  27712   7140 S   1.7   0.2   2:38.21 pipewire-pulse                                                             

```

### - use ps aux I less to open process snapshot in less
```sh
[bohdan@fedora ~]$ ps aux | less
```
![[Pasted image 20221013113510.png]]

### - use '[[cat]] [[I]] [[cut]] -d: -f2' to show 2 column in text file
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

```

### --help
```sh

```

***

## [[OPERATORS]]

***
