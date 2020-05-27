# docker

Test Docker version

```js
$ docker --version
Docker version 19.03.8, build afacb8b
```

## Overview of Docker Compose

Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a `YAML` file to configure your application’s services. Then, with a single command, you create and start all the services from your configuration.

[Get started with Docker Compose](https://docs.docker.com/compose/gettingstarted/)

`docker-compose up`

http://localhost:5000/
Hello World! I have been seen 1 times.

`docker image ls`

## [Build and run your image](https://docs.docker.com/get-started/part2/)

`git clone https://github.com/dockersamples/node-bulletin-board`  
`cd node-bulletin-board/bulletin-board-app`  

Make sure you’re in the directory `node-bulletin-board/bulletin-board-app` in a terminal or PowerShell using the cd command. Let’s build your bulletin board image:

`docker build --tag bulletinboard:1.0`

PS C:\samples\node-bulletin-board> `cd .\bulletin-board-app\`  
PS C:\samples\node-bulletin-board\bulletin-board-app> `docker build --tag bulletinboard:1.0 .`　

Successfully built 441a41f6efc7
Successfully tagged bulletinboard:1.0

Run your image as a container
`docker run --publish 8000:8080 --detach --name bb bulletinboard:1.0`
79e717bef4708c3ef60e2ce457b8aa0e266f41028dec2c7e069133d7d9ba78af

visit your application in a browser at http://localhost:8000/

`docker rm --force bb`  
bb