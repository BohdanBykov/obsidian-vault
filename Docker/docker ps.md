#  Command [[docker ps]] :

***

## About:

### - show containers

***


## Use Cases:

### - use to show running containers
```sh

```

### - use to  show all containers 
```sh
[bohdan@fedora ~]$ docker create -t -i --name test ubuntu:18.04
bb6ec1328f419b00d4ed890237906f3fc63d15918f29e21a3a60ceb9053ad78f
[bohdan@fedora ~]$ docker ps -a
CONTAINER ID   IMAGE           COMMAND       CREATED              NAMES                  
bb6ec1328f41   ubuntu:18.04    "bash"        About a minute ago   test                                                            
```


## Keys:
```sh
Options:
  -a, --all             Show all containers (default shows just running)
  -f, --filter filter   Filter output based on conditions provided
      --format string   Pretty-print containers using a Go template
  -n, --last int        Show n last created containers (includes all states) 
                        (default -1)
  -l, --latest          Show the latest created container (includes all states)
      --no-trunc        Don't truncate output
  -q, --quiet           Only display container IDs
  -s, --size            Display total file sizes

```

### --help
```sh
Usage:  docker ps [OPTIONS]
```

***
