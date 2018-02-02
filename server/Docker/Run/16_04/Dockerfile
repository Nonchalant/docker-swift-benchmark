FROM nonchalant/docker-swift:16.04
MAINTAINER afrontier829@gmail.com

USER root
RUN mkdir -p /server
COPY ./Config /server/Config
COPY ./.build /server/.build

ENV PORT 8080
EXPOSE 8080

WORKDIR /server

CMD ["./.build/debug/Run"]
