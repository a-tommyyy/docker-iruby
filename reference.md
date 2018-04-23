# Docker reference

## HelloWorld!!

```bash
docker-iruby git:(master!?) 🐳 v18.03.0-ce
➜ docker run hello-world
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
9bb5a5d4561a: Pull complete
Digest: sha256:f5233545e43561214ca4891fd1157e1c3c563316ed8e237750d59bde73361e77
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate wors, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/engine/userguide/
 ```

## dockerコマンド
### docker ps
稼働中のコンテナ一覧  
#### オプション 
-a  全てのコンテナ一覧
-q  コンテナIDのみ取得

```bash
docker-iruby git:(master?) 🐳 v18.03.0-ce
➜ docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
docker-iruby git:(master?) 🐳 v18.03.0-ce
➜ docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES
23902fd90107        hello-world         "/hello"            15 minutes ago      Exited (0) 15 minutes ago                       nervous_shockley
docker-iruby git:(master?) 🐳 v18.03.0-ce
➜ docker ps -aq
23902fd90107
```

### docker images
イメージ一覧
#### オプション 
-q  イメージIDのみ取得

```bash
docker-iruby git:(master?) 🐳 v18.03.0-ce
➜ docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
hello-world         latest              e38bc07ac18e        8 days ago          1.85kB
```

### docker rm
コンテナの削除

```bash
docker-iruby git:(master?) 🐳 v18.03.0-ce
➜ docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES
23902fd90107        hello-world         "/hello"            29 minutes ago      Exited (0) 29 minutes ago                       nervous_shockley
docker-iruby git:(master?) 🐳 v18.03.0-ce
➜ docker rm nervous_shockley
nervous_shockley
docker-iruby git:(master?) 🐳 v18.03.0-ce
➜ docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
``` 
### docker rmi
イメージの削除

```bash
docker-iruby git:(master?) 🐳 v18.03.0-ce
➜ docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
hello-world         latest              e38bc07ac18e        8 days ago          1.85kB
docker-iruby git:(master?) 🐳 v18.03.0-ce
➜ docker rmi hello-world
Untagged: hello-world:latest
Untagged: hello-world@sha256:f5233545e43561214ca4891fd1157e1c3c563316ed8e237750d59bde73361e77
Deleted: sha256:e38bc07ac18ee64e6d59cf2eafcdddf9cec2364dfe129fe0af75f1b0194e0c96
Deleted: sha256:2b8cbd0846c5aeaa7265323e7cf085779eaf244ccbdd982c4931aef9be0d2faf
docker-iruby git:(master?) 🐳 v18.03.0-ce
➜ docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
```

### docker pull
イメージの取り込み

```bash
docker-iruby git:(master) 🐳 v18.03.0-ce
➜ docker pull ruby:2.5.1
2.5.1: Pulling from library/ruby
c73ab1c6897b: Pull complete
1ab373b3deae: Pull complete
b542772b4177: Pull complete
57c8de432dbe: Pull complete
1785850988c5: Pull complete
953e617a9c21: Pull complete
09400a4d0988: Pull complete
0775b59c37c3: Pull complete
Digest: sha256:f70114f7b5901a84de89fd9ee93d41f8ed9ea5d9efee6f37e54987d331e3f9a5

docker-iruby git:(master!?) 🐳 v18.03.0-ce
➜ docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
ruby                2.5.1               1624ebb80e3e        3 weeks ago         863MB
```
