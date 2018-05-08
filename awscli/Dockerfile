FROM alpine:edge
LABEL maintainer "Niko Virtala <niko@nikovirtala.io>"

RUN apk --no-cache add \
  ca-certificates \
  groff \
  less \
  python \
  py2-pip \
  && pip install awscli

RUN adduser -D -g '' -h /home/nikovirtala nikovirtala
USER nikovirtala
WORKDIR /home/nikovirtala

RUN mkdir -p /home/nikovirtala/.aws

ENTRYPOINT ["aws"]
