FROM alpine:latest
LABEL maintainer "Niko Virtala <niko@nikovirtala.io>"

RUN apk --no-cache add \
  ca-certificates \
  groff \
  less \
  python \
  py2-pip \
  && pip install awscli \
  && mkdir -p /root/.aws

ENTRYPOINT ["aws"]
