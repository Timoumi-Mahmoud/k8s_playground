## Setup 
```
$ docker volume create cockrov
$ docker volume create -d bridge cockronet

$ docker run -d \
  --name cockroach \
  --hostname db \
  --network cockronet \
  -p 26257:26257 \
  -p 8080:8080 \
  -v cockroachdb:/cockroach/cockroach-data \
  cockroachdb/cockroach:latest-v20.1 start-single-node \
  --insecure
```



```
$ docker exec -it cockroach ./cockroach sql --insecure 
$ create database mydb;
$ create user bara;
$ grant all on database mydb to bara;

```
