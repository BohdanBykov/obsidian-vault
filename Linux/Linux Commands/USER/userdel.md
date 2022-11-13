#  Command [[userdel]] :

***

## About:

### - can remove user

***


## Use Cases:

### - use userdel to delete user without homedir
```sh
[root@fedora ~]# userdel test
[root@fedora ~]# cat /etc/passwd | grep test
[root@fedora ~]# 
```

### - userdel -r to delete user with homedir 
```sh
[root@fedora ~]# userdel -r test
[root@fedora ~]# ls /home
bohdan
[root@fedora ~]# 
```

## Keys:
```sh
Options:
  -f, --force                   force some actions that would fail otherwise
                                e.g. removal of user still logged in
                                or files, even if not owned by the user
  -h, --help                    display this help message and exit
  -r, --remove                  remove home directory and mail spool
  -R, --root CHROOT_DIR         directory to chroot into
  -P, --prefix PREFIX_DIR       prefix directory where are located the /etc/* files
  -Z, --selinux-user            remove any SELinux user mapping for the user
```

### --help
```sh
[root@fedora ~]# userdel --help
Usage: userdel [options] LOGIN
```

***

## [[Linux Commands]]

***
