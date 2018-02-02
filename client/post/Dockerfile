FROM ubuntu:16.04

RUN apt-get -q update && \
    apt-get -q install -y \
    apache2 \
    && rm -r /var/lib/apt/lists/*

RUN mkdir -p /client
COPY ./post.json /client/post.json

WORKDIR /client

CMD ab -s 10000 -n $NUMBER -c $CONCURRENCY -p ./post.json -T 'application/json' -H 'accept: application/json' http://ec2-34-217-46-229.us-west-2.compute.amazonaws.com/posts
