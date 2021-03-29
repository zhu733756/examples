FROM golang:1.15
WORKDIR /

COPY  testmachine.go ./main.go
COPY go.sum ./go.sum
COPY go.mod ./go.mod

ENV GOPROXY=https://goproxy.io,direct
RUN go mod download
RUN go build -o testmachine ./main.go 

CMD ["./testmachine"]
