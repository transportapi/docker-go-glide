# USAGE:
#   # Build image
#   docker build -t go-glide .
#
#   docker run -it \
#     -u $(id -u):$(id -g) \
#     -v `pwd`:/go/src/package/path \
#     go-glide
FROM golang:1.8.0

ARG VERSION=v0.12.3

RUN cd /tmp \
 && wget https://github.com/Masterminds/glide/releases/download/${VERSION}/glide-${VERSION}-linux-amd64.tar.gz \
 && tar xzf glide-${VERSION}-linux-amd64.tar.gz \
 && mv linux-amd64/glide /usr/bin/ \
 && cd ~ \
 && rm -rf /tmp/*
