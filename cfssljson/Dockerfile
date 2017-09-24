FROM alpine:latest
LABEL maintainer "Niko Virtala <niko@nikovirtala.io>"

WORKDIR /root

RUN apk add --no-cache --virtual curl ca-certificates && \
  curl -sSLO https://pkg.cfssl.org/R1.2/cfssljson_linux-amd64 && \
	mv cfssljson_linux-amd64 cfssljson && \
  chmod +x cfssljson

ENTRYPOINT ["/root/cfssljson"]
