# Videogame dockerfile example
# TODO: try volume integration ?

FROM selfsigned/void-vidya-base
LABEL maintainer="selfsigned@protonmail.ch"

RUN xbps-install -Syu tesseract

CMD tesseract

# And then:
# x11docker --gpu --pulseaudio tesseract
# Easy right?
