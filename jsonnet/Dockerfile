FROM golang:latest

RUN apt update

RUN go install github.com/google/go-jsonnet/cmd/jsonnet@latest

RUN go install -a github.com/jsonnet-bundler/jsonnet-bundler/cmd/jb@latest

RUN mkdir -p /home/usr/mnt

WORKDIR /home/user/mnt