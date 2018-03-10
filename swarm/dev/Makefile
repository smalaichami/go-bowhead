.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/smalaichami/go-bowhead/cmd/swarm
	go build -o bin/geth     github.com/smalaichami/go-bowhead/cmd/geth
	go build -o bin/bootnode github.com/smalaichami/go-bowhead/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/smalaichami/go-bowhead/swarm/...
