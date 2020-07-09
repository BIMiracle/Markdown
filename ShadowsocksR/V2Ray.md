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




##v2ray
bash <(curl -L -s https://install.direct/go.sh)

"port": 35383

"id": "2f958737-789f-42dc-ab61-204b1dc241bd"

"alterId": 64


```
# firewalld放行端口（适用于CentOS7/8）
firewall-cmd --permanent --add-port=35383/tcp
# 35383改成你配置文件中的端口号
firewall-cmd --reload

# ufw放行端口（适用于ubuntu）
ufw allow 35383/tcp
# 35383改成你的端口号

# iptables 放行端口（适用于CentOS 6/7）
iptables -I INPUT -p tcp --dport 35383 -j ACCEPT
```

```
# 设置开机启动
systemctl enable v2ray
# 运行v2ray
systemctl start v2ray
```