## Build
FROM nonchalant/docker-swift-build:14.04 as builder

USER root
COPY ./Config /server/Config
COPY ./Sources /server/Sources
COPY ./Package.resolved /server/Package.resolved
COPY ./Package.swift /server/Package.swift

WORKDIR /server
RUN swift build


## Run
FROM nonchalant/docker-swift:14.04

USER root
COPY --from=builder /server/Config /server/Config
COPY --from=builder /server/.build /server/.build

ENV PORT 8080
EXPOSE 8080

WORKDIR /server

CMD ["./.build/debug/Run"]
