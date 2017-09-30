FROM alpine:latest
LABEL maintainer "Niko Virtala <niko@nikovirtala.io>"

WORKDIR /root

RUN apk add --no-cache --virtual curl ca-certificates && \
  stable=$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt) && \
  curl -sSLO https://storage.googleapis.com/kubernetes-release/release/${stable}/bin/linux/amd64/kubectl && \
	chmod +x kubectl && \
  mv kubectl /usr/local/bin/kubectl

ENTRYPOINT ["kubectl"]
