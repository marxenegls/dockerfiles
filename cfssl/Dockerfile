FROM alpine:latest
LABEL maintainer "Niko Virtala <niko@nikovirtala.io>"

WORKDIR /root

RUN apk add --no-cache --virtual curl ca-certificates && \
  curl -sSLO https://pkg.cfssl.org/R1.2/cfssl_linux-amd64 && \
	chmod +x cfssl_linux-amd64 && \
  mv cfssl_linux-amd64 /usr/local/bin/cfssl

ENTRYPOINT ["cfssl"]
