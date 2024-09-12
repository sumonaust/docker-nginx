# Dockerizing a static HTML page using nginx

To build docker images

```
docker build -t <TAG-NAME> .
```

To run docker images

```
docker run -p 8080:80 -d <TAG-NAME>
```


docker ps

-------------

lsb_release -a

sudo apt-get update

sudo apt install docker.io

sudo systemctl enable docker

sudo systemctl status docker

sudo systemctl start docker

sudo docker run hello-world

docker --version