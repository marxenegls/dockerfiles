FROM alpine:edge
LABEL maintainer "Niko Virtala <niko@nikovirtala.io>"

RUN apk add --no-cache --virtual curl ca-certificates && \
  curl -sSLO https://pkg.cfssl.org/R1.2/cfssl_linux-amd64 && \
	chmod +x cfssl_linux-amd64 && \
  mv cfssl_linux-amd64 /usr/local/bin/cfssl

RUN adduser -D -g '' -h /home/nikovirtala nikovirtala
USER nikovirtala
WORKDIR /home/nikovirtala

ENTRYPOINT ["cfssl"]
