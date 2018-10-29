# Docker

```
## imageの取得
$ docker build -t dd_docker:#{tag} (-f path/to/Dockerfile) .
$ docker pull #{imagename}

## imageへの操作
$ docker images
$ docker image rm #{imagename}

## containerの起動
$ docker run -d --name redis redis:3.2.0
$ docker run -d --name app -p 5000:5000 --link redis dd_docker:0.1
# 作業後自動でdocker stop & rm までする
$ docker run --rm -it 

## containerへの操作
$ docker ps
$ docker stop #{container_id}
$ docker rm #{container_id}
$ docker logs #{container_id}
$ docker exec -it #{container_id}
```

# docker-compose

```
$ docker-compose up -d
$ docker-compose ps
$ docker-compose logs (#{container_id})
$ docker-compose stop
$ docker-copmose rm
$ docker-compose build # update image from Dockerfile
```