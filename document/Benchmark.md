# Environment

## Server

- Amazon Ec2 c4.large
- Swift: 4.0.3
- Swift Package Manager: Swift 4.0.0-dev
- Vapor: 2.1.0

## Client

- Amazon Ec2 t2.micro
- Apache Bench


# Benchmark

- [Ubuntu 16.04](https://github.com/Nonchalant/docker-swift-benchmark/blob/master/server/Docker/Run/16_04/Dockerfile)
- [Ubuntu 14.04](https://github.com/Nonchalant/docker-swift-benchmark/blob/master/server/Docker/Run/14_04/Dockerfile)

## Get ([Ubuntu 16.04](https://github.com/Nonchalant/docker-swift-benchmark/wiki/Ubuntu-16.04-GET), [Ubuntu 14.04](https://github.com/Nonchalant/docker-swift-benchmark/wiki/Ubuntu-16.04-GET))

### Concurrency = 10

- Request = 10
- Request = 100
- Request = 1000

### Concurrency = 100

- Request = 100
- Request = 1000
- Request = 10000

### Concurrency = 1000

- Request = 1000
- Request = 10000

## Post ([Ubuntu 16.04](https://github.com/Nonchalant/docker-swift-benchmark/wiki/Ubuntu-16.04-POST), [Ubuntu 14.04](https://github.com/Nonchalant/docker-swift-benchmark/wiki/Ubuntu-16.04-POST))

### Concurrency = 10

- Request = 10
- Request = 100
- Request = 1000

### Concurrency = 100

- Request = 100
- Request = 1000
- Request = 10000

### Concurrency = 1000

- Request = 1000
- Request = 10000
