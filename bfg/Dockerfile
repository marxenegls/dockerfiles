FROM openjdk:8-jre-alpine
LABEL maintainer "Niko Virtala <niko@nikovirtala.io>"

WORKDIR /root

RUN apk add --no-cache --virtual curl ca-certificates && \
  curl -sSLO http://repo1.maven.org/maven2/com/madgag/bfg/1.12.16/bfg-1.12.16.jar && \
  mv bfg-1.12.16.jar /usr/local/bin/bfg.jar

ENTRYPOINT ["java", "-jar", "/usr/local/bin/bfg.jar"]
