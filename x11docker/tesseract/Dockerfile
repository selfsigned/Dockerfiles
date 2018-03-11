# Videogame dockerfile example
# TODO: try volume integration ?

FROM voidlinux/voidlinux
LABEL maintainer="selfsigned@protonmail.ch"

RUN xbps-install -Syu \
	xorg-minimal

# mesa drivers, pick the one you need
RUN xbps-install -Sy mesa-ati-dri mesa-intel-dri tesseract

CMD tesseract
