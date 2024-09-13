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

--------------------
FROM ubuntu
RUN apt update
RUN apt install python3 -y
RUN apt -y install python3-pip
WORKDIR src
COPY . .
RUN pip install -r requirements.txt --break-system-packages
EXPOSE 5000
CMD ["flask", "run", "--host", "0.0.0.0"]

file: app.py  Dockerfile  requirements.txt
------------------------------------------------

FROM node:21-alpine
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["npm", "start"]
