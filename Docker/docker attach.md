#  Command [[docker attach]] :

***

## About:

### - connect container input/output/error stream to your local terminal

***


## Use Cases:

### - use to attach to container
```sh
[bohdan@fedora ~]$ docker ps
CONTAINER ID   IMAGE          COMMAND   CREATED          STATUS         PORTS     NAMES
bb6ec1328f41   ubuntu:18.04   "bash"    29 minutes ago   Up 8 minutes             test
[bohdan@fedora ~]$ docker attach test
root@bb6ec1328f41:/# 
root@bb6ec1328f41:/# exit
exit
[bohdan@fedora ~]$ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
```

### - use to 
```sh

```


## Keys:
```sh
Options:
      --detach-keys string   Override the key sequence for detaching a container
      --no-stdin             Do not attach STDIN
      --sig-proxy            Proxy all received signals to the process (default    
                             true)
```

### --help
```sh
Usage:  docker attach [OPTIONS] CONTAINER
```

***

