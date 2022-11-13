#  Command [[docker pull]] :

***

## About:

### - can download docker image from repository.

***


## Use Cases:

### - use to download ubuntu 18.04 image
```sh
[bohdan@fedora ~]$ docker image list
REPOSITORY           TAG       IMAGE ID       CREATED        SIZE
userdatahelper_bot   latest    265194a071d4   5 weeks ago    939MB
mysql                latest    43fcfca0776d   5 weeks ago    449MB
bbykov/redis_db      latest    fed9ac62e23d   5 weeks ago    117MB
fedora               latest    98ffdbffd207   5 months ago   163MB
[bohdan@fedora ~]$ docker pull ubuntu:18.04
18.04: Pulling from library/ubuntu
e706e0a9f423: Pull complete 
Digest: sha256:40b84b75884ff39e4cac4bf62cb9678227b1fbf9dbe3f67ef2a6b073aa4bb529
Status: Downloaded newer image for ubuntu:18.04
docker.io/library/ubuntu:18.04
[bohdan@fedora ~]$
```

### - use to 
```sh

```


## Keys:
```sh
Options:
  -a, --all-tags                Download all tagged images in the repository
      --disable-content-trust   Skip image verification (default true)
      --platform string         Set platform if server is multi-platform capable
  -q, --quiet                   Suppress verbose output
```

### --help
```sh
Usage:  docker pull [OPTIONS] NAME[:TAG|@DIGEST]
```

***

