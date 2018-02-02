version=16_04

vapor-build:
	docker build -f Docker/Vapor/${version}/Dockerfile -t nonchalant/vapor-build:`echo ${version} | tr _ .` .

build: vapor-build
	docker run nonchalant/vapor-build:`echo ${version} | tr _ .`
	docker cp `docker ps -l -q`:/vapor/.build .
	docker rm `docker ps -l -q`
	docker build -f Docker/Run/${version}/Dockerfile -t nonchalant/vapor-server:`echo ${version} | tr _ .` .

run:
	docker-compose -f Docker/Run/${version}/docker-compose.yml up -d
