build:
	#protoc --go_out=plugins=micro:$(GOPATH)ish2bShippy/consignment-service/ ./proto/consignment/consignment.proto
	docker build -t ish2b/consignment-service .
run:
	docker run -p  50051:50051 -e MICRO_SERVER_ADDRESS=:50051 -e MICRO_REGISTRY=mdns --rm ish2b/consignment-service &
