FROM golang:1.24.4-alpine

# Alpine lacks CGO libraries needed by `controller-gen`
RUN apk add --no-cache build-base

RUN GO111MODULE=on go get sigs.k8s.io/controller-tools/cmd/controller-gen@v0.3.0

RUN mkdir /gatekeeper
WORKDIR /gatekeeper
