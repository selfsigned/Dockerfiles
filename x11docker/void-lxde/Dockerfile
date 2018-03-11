FROM selfsigned/void-vidya-base
MAINTAINER selfsigned@protonmail.ch

RUN xbps-install -Sy \
	lxde \
	ttf-ubuntu-font-family \
	mesa-demos

ENTRYPOINT ["startlxde"]
