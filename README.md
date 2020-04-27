# tftp

To build

```
docker build --rm --tag=robertcsapo/tftp .
```

To run

```
docker run net=host -p 0.0.0.0:69:69/udp -i -t robertcsapo/tftp
```

Mounts the following volume for persistent data

```
/var/tftpboot
```

To map the volume to a host directory

```
docker run net=host -it -p 0.0.0.0:69:69/udp -v /var/tftpboot:/var/tftpboot robertcsapo/tftp
```

To map local directory to the container

```
docker run net=host -it -p 0.0.0.0:69:69/udp -v $PWD:/var/tftpboot robertcsapo/tftp
```

Run temporary in local directory

```
docker run net=host -it --rm -p 0.0.0.0:69:69/udp -v $PWD:/var/tftpboot robertcsapo/tftp
```

Clean up

```
docker rmi robertcsapo/tftp
```
