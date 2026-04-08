---
title: Install Gotosocial with dockers/Gotosocial 搭建教程
date: '2022-12-24 00:00:00'
slug: InstallGotosocialwithdockersGotosocial-da-jian-jiao-cheng
categories:
- 转载
tags:
- 网站
- Python
- docker
- Linux
- Nginx
---
以下教程基于ubuntu 18.4， 其余版本未验证过，不过应该没什么问题。
1. 更新系统：
apt update && apt upgrade -y
2. 安装Docker和Docker Compose
curl -fsSL https://get.docker.com -o get-docker.sh && sh get-docker.sh

3. 安装nginx
apt install nginx -y
4. 下载和修改配置文件
mkdir -p ~/gotosocial/data &&  cd ~/gotosocial &&  chown 1000:1000 data && curl -fsSL https://raw.githubusercontent.com/superseriousbusiness/gotosocial/main/example/docker-compose/docker-compose.yaml -o docker-compose.yaml
5. 然后修改docker-compose.yaml
sed -ri 's/example.org/此处替换为你的域名/g' ~/gotosocial/docker-compose.yaml
6. 把默认映射的443端口改为8080
sed -ri 's/443/8080/g' ~/gotosocial/docker-compose.yaml
7. 初次运行
docker compose up -d
8. 用Nginx反代端口
nano /etc/nginx/conf.d/gotosocial.conf
修改为如下内容
server {
  listen 80;
  listen [::]:80;
  server_name example.org;
  location / {
    proxy_pass http://localhost:8080/;
    proxy_set_header Host $host;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection "upgrade";
    proxy_set_header X-Forwarded-For $remote_addr;
    proxy_set_header X-Forwarded-Proto $scheme;
  }
}
9. 重启NIGIX
systemctl restart nginx
10. 申请SSL 证书
sudo apt install certbot python3-certbot-nginx nginx
sudo certbot --nginx

内容来源：
[https://zhuanlan.zhihu.com/p/531358936?utm_id=0](https://zhuanlan.zhihu.com/p/531358936?utm_id=0)
[https://docs.gotosocial.org/en/latest/installation_guide/docker/](https://docs.gotosocial.org/en/latest/installation_guide/docker/)

---


