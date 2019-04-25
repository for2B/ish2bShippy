FROM ish2b/go-micoroservice as builder

WORKDIR /go/ish2bShippy/vessel-service

RUN go build -o vessel-service main.go

FROM alpine:latest

RUN mkdir /service

WORKDIR /service

COPY --from=builder /go/ish2bShippy/vessel-service/vessel-service .

CMD ["./vessel-service"]
