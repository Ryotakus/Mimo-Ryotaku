# Mimo Ryotaku

## ✨ 项目简介
Mimo Ryotaku 是一个基于 Web 的轻量级 管理服务器集群平台。


## 🏗️ 安装部署
在克隆代码后，通过安装依赖并运行脚本即可快速启动项目：

```shell
git clone https://github.com/cmliu/webssh
cd webssh
pip install -r requirements.txt && python run.py --delay=10 --encoding=utf-8 --fbidhttp=False --maxconn=20 --origin='*' --policy=warning --redirect=False --timeout=10 --port=5731 --debug --xsrf=False --xheaders --wpintvl=1
```

## 💡 工作原理
WebSSH 通过 WebSocket 与浏览器进行实时交互，并将请求转发给基于 Tornado 与 Paramiko 的后端，实现对 SSH 服务器的安全连接和交互。流程如下所示：
```
+---------+     http     +--------+    ssh    +-----------+
| browser | <==========> | webssh | <=======> | ssh server|
+---------+   websocket  +--------+    ssh    +-----------+
```
这使得用户无需本地安装 SSH 客户端，即可通过网页方便快速地完成服务器管理操作。


