FROM ish2b/go-micoroservice as builder

WORKDIR /go/ish2bShippy/consignment-cli

RUN go build -o consignment-cli cli.go

FROM alpine:latest

RUN mkdir /service

WORKDIR /service

COPY --from=builder /go/ish2bShippy/consignment-cli/consignment-cli .
COPY --from=builder /go/ish2bShippy/consignment-cli/consignment.json .

CMD ["./consignment-cli"]
