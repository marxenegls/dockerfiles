FROM openjdk:8-jre-alpine
LABEL maintainer "Niko Virtala <niko@nikovirtala.io>"

WORKDIR /root

RUN apk add --no-cache --virtual curl ca-certificates && \
  _bfgversion=1.12.16 && \
  curl -sSLO http://repo1.maven.org/maven2/com/madgag/bfg/${_bfgversion}/bfg-${_bfgversion}.jar && \
  mv bfg-${_bfgversion}.jar /usr/local/bin/bfg.jar

ENTRYPOINT ["java", "-jar", "/usr/local/bin/bfg.jar"]
