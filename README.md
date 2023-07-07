# how to use gogs install a repo server in mac device?
1. install docker (you can search in google how to install docker)

2. Pull image from Docker Hub.
```shell
docker pull gogs/gogs
```

3. Create local directory for volume.
```shell
mkdir -p /tmp/gogs
```

4. Use `docker run` for the first time.
```shell
docker run --name=gogs -p 10022:22 -p 3000:3000 -v /tmp/gogs:/data gogs/gogs
```

5. Use `docker start` if you have stopped it.
```shell
docker start gogs
```

6. login to dashboard
```shell
http://localhost:3000/
```
you will see below page, you can choose "SQLite3" as databaseType, then click "Install"
![](images/choose_sqllite.png)




