FROM golang:1.20 AS builder
WORKDIR /app
COPY . .
RUN go build -o myapp

FROM alpine
WORKDIR /app
COPY --from=builder /app/myapp ./myapp
CMD ["./myapp"]
