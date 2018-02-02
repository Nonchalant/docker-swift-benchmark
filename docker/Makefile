version=16_04

build-image:
	docker build -f Build/${version}/Dockerfile -t nonchalant/docker-swift-build:`echo ${version} | tr _ .` .

run-image:
	docker build -f Run/${version}/Dockerfile -t nonchalant/docker-swift:`echo ${version} | tr _ .` .
