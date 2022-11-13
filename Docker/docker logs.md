#  Command [[docker logs]] :

***

## About:

### - get logs from the container

***


## Use Cases:

### - use to 
```sh
[bohdan@fedora ~]$ docker logs test
root@bb6ec1328f41:/# exit
root@bb6ec1328f41:/# exit
root@bb6ec1328f41:/# ^C
root@bb6ec1328f41:/# exit
exit
root@bb6ec1328f41:/# exit
[bohdan@fedora ~]$ 
```

### - use to 
```sh

```


## Keys:
```sh
Options:
      --details        Show extra details provided to logs
  -f, --follow         Follow log output
      --since string   Show logs since timestamp (e.g. 2013-01-02T13:23:37Z) or relative (e.g. 42m for 42 minutes)
  -n, --tail string    Number of lines to show from the end of the logs (default "all")
  -t, --timestamps     Show timestamps
      --until string   Show logs before a timestamp (e.g. 2013-01-02T13:23:37Z) or relative (e.g. 42m for 42 minutes)
```

### --help
```sh
Usage:  docker logs [OPTIONS] CONTAINER
```

***
