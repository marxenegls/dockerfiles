FROM alpine:edge
LABEL maintainer "Niko Virtala <niko@nikovirtala.io>"

RUN apk add --no-cache --virtual curl ca-certificates && \
  curl -sSLO https://pkg.cfssl.org/R1.2/cfssljson_linux-amd64 && \
	chmod +x cfssljson_linux-amd64 && \
  mv cfssljson_linux-amd64 /usr/local/bin/cfssljson

RUN adduser -D -g '' -h /home/nikovirtala nikovirtala
USER nikovirtala
WORKDIR /home/nikovirtala

ENTRYPOINT ["cfssljson"]
