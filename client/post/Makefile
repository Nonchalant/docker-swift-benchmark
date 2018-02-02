init:
	sudo service docker start

build:
	docker build -t nonchalant/post:0.1 .

run:
	docker run -e NUMBER=$(NUMBER) -e CONCURRENCY=$(CONCURRENCY) nonchalant/post:0.1
