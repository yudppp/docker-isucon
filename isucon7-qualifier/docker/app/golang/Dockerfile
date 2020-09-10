FROM golang:1.13-alpine

COPY ./src/webapp/go /home/isucon/isubata/webapp/go
WORKDIR /home/isucon/isubata/webapp/go
RUN apk add make gcc g++ git ca-certificates curl libc6-compat

RUN wget -q -O /usr/local/bin/slackcat https://github.com/bcicen/slackcat/releases/download/v1.6/slackcat-1.6-linux-amd64 && \
    chmod +x /usr/local/bin/slackcat

RUN make

EXPOSE 5000

ENTRYPOINT ["/home/isucon/isubata/webapp/go/isubata"]
