FROM golang:1.23-alpine

# Set the working directory
WORKDIR /app

# Install required packages
RUN apk add --no-cache git

# Install Fabric
RUN git clone https://github.com/danielmiessler/fabric.git .

# Copy your Fabric configuration or scripts here
RUN go install github.com/danielmiessler/fabric@latest

# Set Environment variables for Go paths
ENV GOROOT=/usr/local/go
ENV GOPATH=/root/go
ENV PATH=$GOPATH/bin:$GOROOT/bin:/root/.local/bin:/usr/local/bin:$PATH

# Set the default command to run Fabric
CMD ["fabric", "-h"]
