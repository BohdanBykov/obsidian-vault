#  Command [[docker exec]] :

***

## About:

### - run command in active container

***


## Use Cases:

### - use docker exec to run command in container
```sh
[bohdan@fedora ~]$ docker exec test pwd
/
[bohdan@fedora ~]$ 
```

### - use to docker exec -it, to run bash in container 
```sh
[bohdan@fedora ~]$ docker exec -it test bash
root@bb6ec1328f41:/# exit
exit
[bohdan@fedora ~]$ docker ps
CONTAINER ID   IMAGE          COMMAND   CREATED          STATUS         PORTS     NAMES
bb6ec1328f41   ubuntu:18.04   "bash"    38 minutes ago   Up 3 minutes             test
```


## Keys:
```sh
Options:
  -d, --detach               Detached mode: run command in the background
      --detach-keys string   Override the key sequence for detaching a container
  -e, --env list             Set environment variables
      --env-file list        Read in a file of environment variables
  -i, --interactive          Keep STDIN open even if not attached
      --privileged           Give extended privileges to the command
  -t, --tty                  Allocate a pseudo-TTY
  -u, --user string          Username or UID (format: <name|uid>[:<group|gid>])
  -w, --workdir string       Working directory inside the containere
```

### --help
```sh
Usage:  docker exec [OPTIONS] CONTAINER COMMAND [ARG...]
```

***

