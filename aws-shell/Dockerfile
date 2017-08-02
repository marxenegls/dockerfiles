FROM alpine:latest
LABEL maintainer "Niko Virtala <niko@nikovirtala.io>"

RUN apk add --no-cache python && \
    python -m ensurepip && \
    rm -r /usr/lib/python*/ensurepip && \
    pip install --upgrade pip setuptools && \
    rm -r /root/.cache && \
    pip install aws-shell

ENTRYPOINT ["aws-shell"]

