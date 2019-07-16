build:
	# Protobuf gen
	protoc -I. --go_out=plugins=micro:. \
    		proto/consignment/consignment.proto
#	protoc -I. --go_out=plugins=grpc:. \
#	  proto/consignment/consignment.proto
	# Golang Binary creation
	GOOS=linux GOARCH=amd64 go build
	# Docker image build
	sudo docker build -t shippy-service-consignment ./

run:
	# Run the docker image
	sudo docker run -p 50051:50051 \
            -e MICRO_SERVER_ADDRESS=:50051 \
            shippy-service-consignment
