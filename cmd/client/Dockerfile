FROM golang:alpine

WORKDIR /app

COPY go.mod ./
COPY go.sum ./
RUN go mod download

COPY . .

RUN go build -o client ./cmd/client/main.go

CMD ["--help"]
ENTRYPOINT ["./client" ]