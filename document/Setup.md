# Setup

## Required

- docker
- docker-compose

### Linux (RedHat)

```shell
// docker
$ yum install docker

// docker-compose
$ curl -L https://github.com/docker/compose/releases/download/1.18.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose
$ sudo service docker start
```

### Linux (Debian)

```shell
// docker
$ apt-get install docker

// docker-compose
$ curl -L https://github.com/docker/compose/releases/download/1.18.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose
$ sudo service docker start
```

### MacOS

```shell
// docker
$ brew install docker

// docker-compose
$ brew install docker-compose
$ sudo service docker start
```
