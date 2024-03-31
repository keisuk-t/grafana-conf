# Build stage
FROM golang:latest AS builder

WORKDIR /app

COPY . .

RUN go build -o main .

# Run stage
FROM golang:latest

WORKDIR /app

COPY --from=builder /app/main /app/main

CMD ["./main"]