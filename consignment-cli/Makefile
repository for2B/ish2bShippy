build:
	#protoc --go_out=plugins=micro:$(GOPATH)ish2bShippy/consignment-service/ ./proto/consignment/consignment.proto
	docker build -t ish2b/consignment-cli .
run:
	docker run -e MICRO_REGISTRY=mdns --rm ish2b/consignment-cli 
