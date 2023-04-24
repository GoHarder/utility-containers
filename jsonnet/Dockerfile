FROM golang:latest

RUN apt-get update

RUN go install github.com/google/go-jsonnet/cmd/jsonnet@latest
RUN go install -a github.com/jsonnet-bundler/jsonnet-bundler/cmd/jb@latest
RUN go install github.com/brancz/gojsontoyaml@latest

ADD build /usr/local/bin/build
RUN chmod u+x /usr/local/bin/build

WORKDIR /mnt