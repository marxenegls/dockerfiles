FROM alpine:edge
LABEL maintainer "Niko Virtala <niko@nikovirtala.io>"

RUN adduser -D -g '' -h /home/nikovirtala nikovirtala

USER nikovirtala
WORKDIR /home/nikovirtala

RUN apk add --no-cache --virtual curl ca-certificates && \
  stable=$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt) && \
  curl -sSLO https://storage.googleapis.com/kubernetes-release/release/${stable}/bin/linux/amd64/kubectl && \
	chmod +x kubectl && \
  mv kubectl /usr/local/bin/kubectl

ENTRYPOINT ["kubectl"]
