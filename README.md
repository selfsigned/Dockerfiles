# My Dockerfiles
Just a bunch of dockerfiles I made for my own convenience or to mess around.
[My docker hub page](https://hub.docker.com/u/selfsigned/)

## Weechat
### Usage
`docker run -it --name weechat -e TZ="UTC" -v /path/to/your/local/.weechat:/home/weechat/.weechat -p 9001:9001 selfsigned/weechat-void-otr`
### Misc
I included a wrapper to attach to the container as an user that's not in the __docker__ group, put it in your $PATH or /usr/bin and add the following to /etc/sudoers:
`youruser ALL=(root) NOPASSWD /usr/bin/weechat_wrapper`

## x11docker
Dockerfiles for [x11docker](https://github.com/mviereck/x11docker)
