# gRPC Example

In Golang.

## Pre-requisites

Make sure you have protocol buffer compiler and proto go package. Follow this document if you haven't done so:

https://github.com/IronCore864/protobuf-example

## Build

### Run `protoc` command (with the grpc plugin):

```
protoc -I helloworld/ helloworld/helloworld.proto --go_out=plugins=grpc:helloworld
```

### Build Server

```
cd server
go build
```

### Build Client

```
cd client
go build
```

## Run

Start server in the background:

```
cd server
./server &
```

Start client:

```
cd client
./client
```

To quit server:

```
fg
ctrl + c
```
