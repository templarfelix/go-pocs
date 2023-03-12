FROM golang:buster AS builder
WORKDIR /build
COPY go.mod ./
COPY go.sum ./
COPY *.go ./
RUN go build -o main main.go && mv main /main
RUN ls -la

FROM gcr.io/distroless/base-debian11
WORKDIR /
COPY --from=builder /main /main
ENTRYPOINT ["./main"]