FROM alpine

RUN apk update && apk upgrade
RUN apk add tor

RUN adduser -S user
USER user

EXPOSE 9050

ENTRYPOINT ["tor", "--SocksPort", "0.0.0.0:9050"]
