FROM nonchalant/docker-swift-build:16.04
MAINTAINER afrontier829@gmail.com

USER root
RUN mkdir -p /vapor
COPY ./Config /vapor/Config
COPY ./Sources /vapor/Sources
COPY ./Package.resolved /vapor/Package.resolved
COPY ./Package.swift /vapor/Package.swift

WORKDIR /vapor
RUN swift build
