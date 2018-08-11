# v2ray-heroku
> 部署
# 点击 [![](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/xuiv/v2ray-heroku)，[一键部署到heroku](https://heroku.com/deploy?template=https://github.com/xuiv/v2ray-heroku)

客户端config.json设置如下：
```
{
  "log": {
    "loglevel": "warning"
  },
  "inbound": {
    "port": 1080,
    "listen": "127.0.0.1",
    "protocol": "socks",
    "domainOverride": ["tls","http"],
    "settings": {
      "auth": "noauth",
      "udp": false
    }
  },
  "outbound": {
    "protocol": "vmess",
    "settings": {
      "vnext": [{
        "address": "v2-aoxuanheng.herokuapp.com",
        "port": 443,
        "users": [{
          "id": "a9c8f63f-08a1-460b-8286-3830e0eac453",
          "alterId": 64
        }]
      }]
    },
    "streamSettings": {
      "network": "ws",
      "security": "tls"
    }
  }
}
```
