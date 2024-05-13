FROM golang:1.22.3-alpine

COPY todo_app /go/todo_app/

RUN mkdir -p /usr/local/go/src/web/todo_app

WORKDIR /usr/local/go/src/web/todo_app/

RUN apk update \
&& apk add --no-cache git \
&& go mod tidy \
#&& go mod init todo_app \
&& apk add git

EXPOSE 8080