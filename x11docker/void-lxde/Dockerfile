FROM voidlinux/voidlinux
MAINTAINER selfsigned@protonmail.ch

RUN xbps-install -Syu \
	lxde \
	xorg-minimal

# Unicode locale
RUN printf "en_US.UTF-8 UTF-8\nja_JP.UTF-8 UTF-8\n" > /etc/default/libc-locales \
	&& xbps-reconfigure -f glibc-locales

ENV LANG en_US.UTF-8
ENV LC_ALL en_US.UTF-8

# mesa drivers, pick the one you need
RUN xbps-install -Sy mesa-ati-dri mesa-intel-dri

# Fonts and useful stuff
RUN xbps-install -Sy \
	ttf-ubuntu-font-family \
	mesa-demos

ENTRYPOINT ["startlxde"]
