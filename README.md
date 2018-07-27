# Docker Asterisk

Docker images of Asterisk 13, 14 or 15 based on Centos 7 image.

It is clean Asterisk without FastAGI which should run in separate containers.

Because of huge port range requirement of asterisk RTP ports it is recommended to run in with parameter `--network host` instead of port mapping

### Usage

Basic usage

```shell
docker run -d --name asterisk --network=host autor69/asterisk-centos
```

In order to use your own configuration files mount them into standard foler /etc/asterisk folder

```shell
docker run -d --name asterisk \
              --network=host \
              -v /etc/asterisk:/etc/asterisk
autor69/asterisk-centos
```

#### Logging into Asterisk Console
Basic usage

```shell
docker exec -it asterisk asterisk -rvvvvvvvvv
```

You can add alias into your `.bashrc`:

```
alias rasterisk='docker exec -it asterisk asterisk -rvvvvvvvvvv'
```

And then just use command `rasterisk`

## Authors

* **Autor69** - [Autor69](https://github.com/Autor69)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
