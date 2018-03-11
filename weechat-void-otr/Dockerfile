FROM voidlinux/voidlinux
MAINTAINER selfsigned@protonmail.ch

ENV LANG en_US.UTF-8
ENV LC_ALL en_US.UTF-8

RUN xbps-install -Syu
RUN xbps-install -Sy weechat \
weechat-python python-pip python-devel gcc
# installing python-potr for the otr.py script
RUN pip install python-potr websocket-client

# Unicode locale
RUN echo "en_US.UTF-8 UTF-8" > /etc/default/libc-locales
RUN xbps-reconfigure -f glibc-locales

# Setting up an user
RUN useradd -m weechat
USER weechat
WORKDIR /home/weechat

# Relay port
EXPOSE 9001

ENTRYPOINT ["weechat"]
