FROM alpine:latest
LABEL maintainer "Niko Virtala <niko@nikovirtala.io>"

WORKDIR /root

RUN apk add --no-cache --virtual curl ca-certificates && \
  curl -sSLO https://github.com/stedolan/jq/releases/download/jq-1.5/jq-linux64 && \
	chmod +x jq-linux64 && \
  mv jq-linux64 /usr/local/bin/jq

ENTRYPOINT ["jq"]
