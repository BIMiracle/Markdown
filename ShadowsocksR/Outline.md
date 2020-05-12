# Outline Server
## 一、install and run Shadowbox

```
sudo bash -c "$(wget -qO- https://raw.githubusercontent.com/Jigsaw-Code/outline-server/master/src/server_manager/install_scripts/install_server.sh)"
```

备用地址

```
sudo bash -c "$(wget -qO- https://raw.githubusercontent.com/tryEvething/outline-server/master/src/server_manager/install_scripts/install_server.sh)"
```


安装docker报错

```
> Verifying that Docker is installed .......... NOT INSTALLED
> Would you like to install Docker? This will run 'curl -sS https://get.docker.com/ | sh'. [Y/n] y
> Installing Docker ........................... Docker installation failed, please visit https://docs.docker.com/install for instructions.

Sorry! Something went wrong. If you can't figure this out, please copy and paste all this output into the Outline Manager screen, and send it to us, to see if we can help you.
```
[https://www.runoob.com/docker/centos-docker-install.html](https://www.runoob.com/docker/centos-docker-install.html)

安装Docker出现package docker-ce-3:19.03.8-3.el7.x86_64 requires containerd.io >= 1.2.2-3

	yum install https://download.docker.com/linux/fedora/30/x86_64/stable/Packages/containerd.io-1.2.6-3.3.fc30.x86_64.rpm

	
如果出现docker: Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running?.

解决方法:[https://github.com/Jigsaw-Code/outline-server/issues/39](https://github.com/Jigsaw-Code/outline-server/issues/39)

重启Docker
```sudo service docker restart```



## 二、防火墙过滤
成功后会返回

	{"apiUrl":"https://202.133.103.104:18728/O4FZIhyzunCAv2bRlSDGAA","certSha256":"561AE392E3B02EE4AB5989CFCEAF4BAD22BC5827AD6400CE2FC9A64C2A394220"}

保存下来,还有一句提示

	Make sure to open the following ports on your firewall, router or cloud provider:
	- Management port 18728, for TCP
	- Access key port 1175, for TCP and UDP

按照提示终端输入

```
firewall-cmd --zone=public --add-port=37720/tcp --permanent
firewall-cmd --zone=public --add-port=14896/tcp --permanent
firewall-cmd --zone=public --add-port=14896/udp --permanent
firewall-cmd --reload
```

[官方提示配置(未成功)](https://github.com/Jigsaw-Code/outline-server/issues/97)

添加防火墙端口后查看是否已开放:

```
firewall-cmd --list-ports
```

## 三、连接服务器
[下载服务端软件](https://github.com/Jigsaw-Code/outline-releases/tree/master/manager)

选择自定义服务器
![](./pictures/30548CB9-BFBE-4FC7-89D4-2D365AA42430.png)

选择第二项输入之前生成的“apiUrl”，“certSha256”
![](./pictures/QQ20190926-140628@2x.png)


新用户首次充值可能需要 24 小时的账户验证期，耐心等待即可。

添加Key然后[下载客户端使用](https://getoutline.org/zh-CN/home)