
# v2ray 部署在 openshift starter
openshift: 内存设置为256M，每 project 可配置 4 Pods。

Docker 镜像搜索：doudoubing/cundang
（fork于wangyi2005/v2ray修改前）

环境变量： CONFIG_JSON（配置）、

用notepad++将上述变量中 \r\n 替换为\\n，变成一行，导入容器。

客户端： android Actinium、windows v2ray 可用同一个服务端。





点击 Image Name，输入 ggsjj/openshift ，然后点击搜索。

搜索完成之后往下拉一点，找到下图位置，在Name那里填写CONFIG_JSON,在Value位置填写V2ray的配置信息，

Ps：UUID的生成点这里：www.uuidgenerator.net





```bash

{
  "log": {
    "loglevel": "warning"
  },
  "inbound": {
    "protocol": "vmess",
    "port": 8080,
    "settings": {
      "clients": [
        {
          "id": "2f20965e-185d-42cb-aa1b-26941c4c59d2",
          "alterId": 64,
          "security": "aes-128-gcm"
        }
      ]
    },
    "streamSettings": {
      "network": "ws"
    }
  },
  "inboundDetour": [],
  "outbound": {
    "protocol": "freedom",
   "settings": {}
  }
}

```


