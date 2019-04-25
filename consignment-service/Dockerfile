FROM ish2b/go-micoroservice as builder

WORKDIR /go/ish2bShippy/consignment-service

RUN go build -o consignment-service main.go

FROM alpine:latest

RUN mkdir /service

WORKDIR /service

COPY --from=builder /go/ish2bShippy/consignment-service/consignment-service .

CMD ["./consignment-service"]
