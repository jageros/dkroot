# dockerfile
## docker安装
* Centos 7.9
* [Docker官方文档](https://docs.docker.com/engine/install/centos/)
```shell
# 移除已安装的docker软件以及依赖
sudo yum remove docker docker-client docker-client-latest docker-common docker-latest docker-latest-logrotate docker-logrotate docker-engine

# 安装yum工具
sudo yum install -y yum-utils

# yum-config-manager依赖python2， python连接到python2.7
sudo rm -f /usr/bin/python # 删除旧的link
sudo ln /usr/bin/python2.7 /usr/bin/python # 建立新的link

# 增加docker yum源
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

# 安装docker
sudo yum install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# 启动docker
sudo systemctl start docker

# 设置开机启动
sudo systemctl enable docker
```

## 创建Docker网络
``docker network create -d bridge fox-net``

## docker-compose文件
* MySQL
* Redis
* Nginx
* Etcd
* kafka
* MongoDB
* Jenkins
* MiniDoc
* Nexus3