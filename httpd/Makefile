# Note: the "-" in front of the command signifies that the Makefile should continue even if this command returns an error
rerun:
	- docker stop httpd
	- docker rm httpd
	- docker rmi httpd-hardened:latest
	docker build -t httpd-hardened .
	docker run -d --name httpd -p 8080:80 httpd-hardened

stop:
	docker stop httpd
	docker rm httpd
