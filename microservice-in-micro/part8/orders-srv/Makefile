GOPATH:=$(shell go env GOPATH)

.PHONY: build
build: proto
	GOOS=linux GOARCH=amd64 CGO_ENABLED=0 go build -o orders-srv main.go plugin.go

.PHONY: docker
docker:docker
	docker build . -t orders-srv:latest
