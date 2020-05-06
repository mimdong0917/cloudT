# cloudT
Nginx install

# Building & Running

Copy the sources to your docker host and build the container, and to run.
```
	docker build --rm -t mimdong/ubuntu .
	docker run -it --name n1 -p 8888:80 mimdong/ubuntu
