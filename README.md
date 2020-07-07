# Docker Nginx Demo

### Running on Nginx

**1. Run in Nginx Container**

```shell
cd ~/websites/docker_nginx_demo/

docker container run -d -p 8080:80 -v $(pwd):/usr/share/nginx/html --name nginx-demo nginx
```

http://localhost:8080/


**2. Run as Docker Image**

```shell
cd ~/websites/docker_nginx_demo/

docker image build -t nginx-website .

docker container run -d -p 8080:80 nginx-website
```

http://localhost:8080/
