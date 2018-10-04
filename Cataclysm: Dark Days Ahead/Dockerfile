FROM alpine as builder

RUN apk --no-cache add git \
	g++ make\
	ncurses-libs ncurses-dev

RUN git clone https://github.com/CleverRaven/Cataclysm-DDA /cdda
WORKDIR /cdda

RUN make cataclysm -j8 RELEASE=1 LOCALIZE=0

# Final stage
FROM alpine

RUN apk --no-cache add ncurses-libs libgcc libstdc++

RUN adduser -D cataclysm
USER cataclysm

WORKDIR /home/cataclysm
RUN mkdir -p .cataclysm-dda

COPY --from=builder /cdda/cataclysm .
COPY --from=builder /cdda/data ./data

VOLUME ["/home/cataclysm/.cataclysm-dda"]
CMD ["./cataclysm"]
