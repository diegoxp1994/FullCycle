FROM golang:1.23.1-alpine AS builder
WORKDIR /app
COPY go.mod .
COPY hello.go .
RUN CGO_ENABLED=0 GOODS=linux go build -o desafioGo

FROM scratch
COPY --from=builder /app/desafioGo /
ENTRYPOINT [ "/desafioGo" ]

