FROM python:2.7-alpine
LABEL maintainer "Niko Virtala <niko@nikovirtala.io>"

WORKDIR /root

RUN apk add --no-cache --virtual .build-dependencies \
  ca-certificates curl tar openssh-client git \
  && curl -sSLO https://dl.google.com/dl/cloudsdk/release/google-cloud-sdk.tar.gz \
  && tar -zxvf google-cloud-sdk.tar.gz \
  && rm -f google-cloud-sdk.tar.gz \
  && ( \
    cd google-cloud-sdk \
    && ./install.sh \
    --usage-reporting false \
    --path-update true \
  ) \
  && apk del .build-dependencies

ENV PATH $PATH:/root/google-cloud-sdk/bin

ENTRYPOINT ["gcloud"]
