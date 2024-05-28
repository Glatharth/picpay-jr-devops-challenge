FROM golang:1.16
WORKDIR /app
COPY go.mod go.sum ./
RUN go mod download && go mod verify
ADD . .
RUN go build -v -o /usr/local/bin/app

EXPOSE 8080
CMD ["app"]