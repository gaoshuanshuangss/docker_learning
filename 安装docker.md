安装docker

1.先更新系统，并安装相关依赖包，让apt可以通过https访问存储库

sudo apt update

```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

 2,添加docker官方的GPG证书

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

 3.写入软件源信息

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

4.更新源

sudo apt update

5.安装最新版本的 Docker CE

sudo apt install -y docker-ce

6.查看 Docker 服务状态

systemctl status docker

7.启动 Docker

sudo systemctl start docker

8.Docker 开机启动

sudo systemctl enable docker

9.运行 Docker helloworld

\# 查看 Docker 版本信息

sudo docker version

\# 运行 Docker helloworld

sudo docker run hello-world

\# 查看 Docker 容器状态

sudo docker ps