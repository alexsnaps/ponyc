FROM alpine

ENV LLVM_VERSION 5

RUN apk update \
  && apk upgrade \
  && apk add --update \
  alpine-sdk \
  binutils-gold \
  llvm${LLVM_VERSION} \
  llvm${LLVM_VERSION}-dev \
  libexecinfo-dev \
  coreutils \
  linux-headers \
  zlib-dev \
  ncurses-dev \
  bash \
  curl

# add user pony in order to not run tests as root
RUN adduser -D -s /bin/sh -h /home/pony -g root pony
USER pony
WORKDIR /home/pony
