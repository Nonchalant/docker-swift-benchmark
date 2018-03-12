version=16_04

build:
	docker build -f Docker/${version}/Dockerfile -t nonchalant/vapor-server:`echo ${version} | tr _ .` .

run:
	docker-compose -f Docker/${version}/docker-compose.yml up -d
