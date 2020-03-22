1. 打开docker 并且映射本地目录
```
docker run -t -i -p 3458:3458 -v /Users/mickey/Desktop/02project/01en-web:/app -w /app registry.gz.cvte.cn/library/node:8.9.3 /bin/bash
```
2. 查看docker容器运行状态
```
docker ps
```
3. 进入正在运行的容器
```
docker exec -i -t d0d3e3dd419d bash
```
4. 查看docker拥有的镜像
```
docker images
```
5. 查看容器的系统版本信息
```
sudo lsb_release -a
```
6. 修改已有镜像，并且保存： 
```
sudo docker commit -m "add nvm node" -a "add node" fc8dc0021568 node/nvm:latest
```
7. 删除镜像：

8. 打开 docker ：
```
docker run -t -i ouruser/sinatra:nvm /bin/bash
```
9. 下载镜像
```
docker image pull registry.gz.cvte.cn/library/node:8.9.3
```

参考资料

docker http://www.ruanyifeng.com/blog/2018/02/docker-tutorial.html

修改已有镜像、并且保存：https://blog.csdn.net/ling811/article/details/53817123

