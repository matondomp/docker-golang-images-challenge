FROM golang as builder

WORKDIR /usr/src/app

RUN go mod init myapp 

COPY . .

ENTRYPOINT [ "go", "run","."]

FROM golang:1.20rc1-alpine3.17

WORKDIR /usr/src/app

COPY --from=builder /usr/src/app .

EXPOSE 10000

CMD [ "go", "run","." ]
