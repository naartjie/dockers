FROM alpine:3.8
LABEL author="Marcin Jekot"

ARG UP_VERSION=0.8.1

RUN apk update && apk add ca-certificates && rm -rf /var/cache/apk/*

WORKDIR /opt

ADD https://github.com/apex/up/releases/download/v${UP_VERSION}/up_${UP_VERSION}_linux_amd64.tar.gz /opt
RUN tar -xf ./up_${UP_VERSION}_linux_amd64.tar.gz
RUN mv ./up /usr/local/bin
RUN rm -rf /opt

WORKDIR /
ENTRYPOINT [ "/usr/local/bin/up" ]
