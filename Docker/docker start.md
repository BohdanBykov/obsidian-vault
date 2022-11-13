#  Command [[docker start]] :

***

## About:

### - start containers

***

## Use Cases:

### - use to 
```sh
[bohdan@fedora ~]$ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
[bohdan@fedora ~]$ docker start test
test
[bohdan@fedora ~]$ docker ps
CONTAINER ID   IMAGE          COMMAND   CREATED          STATUS         PORTS     NAMES
bb6ec1328f41   ubuntu:18.04   "bash"    21 minutes ago   Up 2 seconds             test
[bohdan@fedora ~]$
```

### - run container and save id in file
```sh
[bohdan@fedora ~]$ docker run --cidfile /tmp/atest ubuntu echo 'done'
done
[bohdan@fedora ~]$ ls /tmp
atest
```

### - run container and save id in file
```sh
[bohdan@fedora ~]$ docker run --cidfile /tmp/atest ubuntu echo 'done'
done
[bohdan@fedora ~]$ ls /tmp
atest
```


## Keys:
```sh
Options:
  -a, --attach               Attach STDOUT/STDERR and forward signals
      --detach-keys string   Override the key sequence for detaching a container
  -i, --interactive          Attach container's STDIN
```

### --help
```sh
Usage:  docker start [OPTIONS] CONTAINER [CONTAINER...]
```

***
