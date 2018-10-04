FROM alpine

RUN apk --no-cache add tor

RUN adduser -S user
USER user

EXPOSE 9050

ENTRYPOINT ["tor", "--SocksPort", "0.0.0.0:9050"]
