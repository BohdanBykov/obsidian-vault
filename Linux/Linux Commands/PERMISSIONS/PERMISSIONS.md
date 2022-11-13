# Linux Permissions

***

##  | General

***

- You can see permissions in folder using [[ls]] command:
```sh
[bohdan@fedora testdirectory]$ ls -l
total 24
drwxr-xr-x. 1 bohdan bohdan    60 Oct 13 11:29 dirtest
-rwxr-----. 1 bohdan bohdan    48 Oct  8 20:29 permissions.txt
-rw-r--r--. 1 bohdan bohdan 14097 Oct  9 10:49 ps2.txt
-rw-r--r--. 1 bohdan bohdan    20 Oct 13 12:27 test.txt
[bohdan@fedora testdirectory]$ 

```

#### Permissions shown in the first column, they have simple schema:
- 1)|-| 2)|---| 3)|---| 4)|---|

1)section show is it a directory
2)section is u-user permissions
3)section is g-group permissions
4)section is o-other permissions to this file. 

#### Unix systems has 3 type of permissions:
- rwx

r)  read
w) write
x) execute

### Also unix system has numeric permission view:

- 0 ---
- 1 --x
- 2 -w-
- 3 -wx
- 4 r--
- 5 r-x
- 6 rw-
- 7 rwx

#### Most usable combinations:
- 740 - owner all, owner group read, everyone else nothing
- 640 - owner read and write, OG read, EE nothing

*** 

## | Example:

***

```sh
drwxr-xr-x. 1 bohdan bohdan    60 Oct 13 11:29 dirtest
```
- in 1) section we see 'd' so this is a directory
- in 2) section we see 'rwx' it means owner can read, write and execute this dir
- in 3) section we see 'r-x' it means owner group can't rewrite this dir
- in 4) section we see 'r-x' so everyone else can't write but also can read and execute

***

## [[Linux Commands]]

***
