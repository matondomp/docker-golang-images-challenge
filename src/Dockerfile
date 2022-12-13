
FROM golang:1.15 as builder

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY go.mod .
#COPY go.sum .

ENV GOPROXY https://proxy.golang.org,direct

RUN go mod download

COPY . .

ENV CGO_ENABLED=0

RUN GOOS=linux go build -ldflags "-s -w" ./main.go

FROM scratch

WORKDIR /usr/src/app

COPY --from=builder /usr/src/app/main .

CMD ["/usr/src/app/main"]