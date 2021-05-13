#配置一


##v2ray带伪装脚本

bash <(curl -sL https://raw.githubusercontent.com/tryEvething/Markdown/master/ShadowsocksR/v2ray.sh)

前往
[https://www.namesilo.com/account_domain_manage_dns.php](https://www.namesilo.com/account_domain_manage_dns.php)
配置HOST解析


|  HOSTNAME   | ADDRESS / VALUE  |  TTL   |
|  ----  | ----  |  ----  |
| www  | 填写服务器地址 |  3600  |

先输入主机名www.bimiracle.top
然后输入个随机路径
/nGUZrXvb09KoyXV


#配置二

推荐系统 Debian 8.7

首先下载脚本

	wget https://install.direct/go.sh

备用地址:

	wget https://raw.githubusercontent.com/tryEvething/Markdown/master/ShadowsocksR/v2rayCore.sh

执行脚本安装 V2Ray

	sudo bash go.sh

启动 V2Ray
	
	sudo systemctl start v2ray

更多用法
	bash go.sh -h

升级更新

	sudo bash go.sh



#other

Mac程序:
[https://github.com/yanue/V2rayU/wiki/V2rayU%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E](https://github.com/yanue/V2rayU/wiki/V2rayU%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E)


[Caddy+h2脚本:](https://github.com/dylanbai8/V2Ray_h2-tls_Website_onekey)
```wget -N --no-check-certificate git.io/h.sh && chmod +x h.sh && bash h.sh```