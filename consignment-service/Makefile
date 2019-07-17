build:
	# Protobuf gen
	protoc -I. --go_out=plugins=micro:. \
    		proto/consignment/consignment.proto
	# Docker image build
	sudo docker build -t shippy-service-consignment ./

run:
	# Run the docker image
	sudo docker run -p 50051:50051 \
            -e MICRO_SERVER_ADDRESS=:50051 \
            shippy-service-consignment
