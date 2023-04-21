FROM golang:latest

RUN apt update

RUN go install github.com/google/go-jsonnet/cmd/jsonnet@latest
RUN go install -a github.com/jsonnet-bundler/jsonnet-bundler/cmd/jb@latest
RUN go install github.com/brancz/gojsontoyaml@latest

WORKDIR /home

RUN bash -c 'mkdir -p {bin,mnt}'

ENV PATH "$PATH:/home/bin"

COPY ./build ./bin/build

# RUN bash -c 'mkdir -p {bin,tmp,mnt}'

# COPY ./build ./tmp/build

# RUN mv ./tmp/build ./bin/build &&\
#    chmod -R 777 /home/bin

WORKDIR /home/mnt