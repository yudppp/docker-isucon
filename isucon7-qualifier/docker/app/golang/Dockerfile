FROM golang:latest

ADD ./src/webapp/go/ /home/isucon/isubata/webapp/go/
WORKDIR /home/isucon/isubata/webapp/go

RUN apt-get -y update && apt-get -y install graphviz

RUN wget -q -O /usr/local/bin/slackcat https://github.com/bcicen/slackcat/releases/download/v1.6/slackcat-1.6-linux-amd64 && \
    chmod +x /usr/local/bin/slackcat

EXPOSE 5000

CMD GOPATH=/home/isucon/isubata/webapp/go go run /home/isucon/isubata/webapp/go/src/isubata/app.go
