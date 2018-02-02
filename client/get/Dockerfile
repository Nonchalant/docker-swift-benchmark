FROM ubuntu:16.04

RUN apt-get -q update && \
    apt-get -q install -y \
    apache2 \
    && rm -r /var/lib/apt/lists/*

CMD ab -n $NUMBER -c $CONCURRENCY http://ec2-34-217-46-229.us-west-2.compute.amazonaws.com/hello
