FROM ubuntu:16.04
MAINTAINER afrontier829@gmail.com

# Install related packages
RUN apt-get -q update && \
    apt-get -q install -y \
    curl \
    libcurl4-openssl-dev \
    libedit-dev \
    libicu-dev \
    libxml2 \
    && rm -r /var/lib/apt/lists/*

# Everything up to here should cache nicely between Swift versions, assuming dev dependencies change little
ARG SWIFT_PLATFORM=ubuntu16.04
ARG SWIFT_BRANCH=swift-4.0.3-release
ARG SWIFT_VERSION=swift-4.0.3-RELEASE

ENV SWIFT_PLATFORM=$SWIFT_PLATFORM \
    SWIFT_BRANCH=$SWIFT_BRANCH \
    SWIFT_VERSION=$SWIFT_VERSION

# Download Swift package, then unpack, cleanup and execute permissions for foundation libs
RUN SWIFT_URL=https://swift.org/builds/$SWIFT_BRANCH/$(echo "$SWIFT_PLATFORM" | tr -d .)/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz \
    && curl -fSsL $SWIFT_URL -o swift.tar.gz \
    && tar -xzf swift.tar.gz --directory / --strip-components=1 \
    && rm -r swift.tar.gz \
    && chmod -R o+r /usr/lib/swift
