# Docker Asterisk

Docker files of Asterisk 13,14 or 15 based on Centos 7 image.

It is clean asterisk without FastAGI or ARI Http server which should run in separate containers.

Because of huge port range requirement of asterisk RTP ports it is recommended to run in with parameter `--network host`


