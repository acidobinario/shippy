FROM debian:latest

RUN mkdir -p /app
WORKDIR /app

ADD consignment.json /app/consignment.json
#ADD consignment2.json /app/consignment2.json
ADD consignment-cli /app/consignment-cli

CMD ["./consignment-cli"]
#CMD ["./shippy-cli-consignment consignment2.json"]
