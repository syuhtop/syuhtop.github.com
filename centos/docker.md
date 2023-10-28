Centos7 安装Docker

```bash
yum makecache
yum install bash-completion -y
bash
yum repolist

# 安装一些必要的工具
yum install -y yum-utils device-mapper-persistent-data lvm2

yum-config-manager --add-repo http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo

yum provides docker-ce

yum install docker-ce -y

docker info

# 启动
systemctl start docker
systemctl enable docker.service

docker ps

curl -o /etc/yum.repos.d/epel.repo http://mirrors.aliyun.com/repo/epel-7.repo

yum makecache fast

yum provides docker-compose

[root@localhost nginx]# touch docker-compose.yml
[root@localhost nginx]# vim docker-compose.yml 
[root@localhost nginx]# docker-compose pull

[root@localhost nginx]# docker-compose up -d
[root@localhost nginx]# docker-compose ps


[root@localhost nginx]# curl -I 127.0.0.1:80
HTTP/1.1 200 OK
Server: nginx/1.23.4
Date: Wed, 24 May 2023 18:33:28 GMT
Content-Type: text/html
Content-Length: 615
Last-Modified: Tue, 28 Mar 2023 15:01:54 GMT
Connection: keep-alive
ETag: "64230162-267"
Accept-Ranges: bytes



https://www.bilibili.com/video/BV1y44y187Bj/?spm_id_from=333.337.search-card.all.click&vd_source=e7ce48abe21938ea89b2dcd43a1f5cc8

```

