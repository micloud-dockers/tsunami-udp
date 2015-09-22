# Tsunami UDP image

## Rebuild image

```
$ cd [Dockerfile-folder]
$ docker build -t [tag-name] .
```

## Start Server Container

Service neet to start in UDP mode, so the port mapping should specify the UDP.

```
$ docker run -it -p 3000:3000/udp peihsinsu/tsunami-udp bash
```


## Start Server


```
[root@dfb42232]# cd $your-project
[root@dfb42232]# tsunamid --port 3000 *
```

## Start Client Container

```
$ docker run -it -p 4000:4000/udp peihsinsu/tsunami-udp bash
```

## Start Client

```
tsunami connect [your.ip.address] [port] set udpport 4000 get [filename] quit
```

ex: 

```
# tsunami connect 123.123.123.123 3000 set udpport 4000 get openSUSE-11.2-GNOME-LiveCD-x86_64.iso quit
```


