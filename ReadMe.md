# TG-EFB-Wechat-Docker

EFB-WeChat的Docker部署方式

- [EH Forwarder Bot](https://github.com/ehForwarderBot/ehForwarderBot) : 2.1.1
- [EFB Telegram Master Channel](https://github.com/ehforwarderbot/efb-telegram-master) : 2.2.4
- [EFB WeChat Slave Channel](https://github.com/ehForwarderBot/efb-wechat-slave) : 2.0.5

## 使用

### 配置

根据提示进行配置，`/root/wechat/config`为配置文件目录

```bash
docker run --rm -it --name="efb-wechat" -v /root/wechat/config:/app/config xzsk2/efb-wechat-docker:latest efb-wizard
```

### 运行

```bash
docker run -d --restart=always --name="efb-wechat" -v /root/wechat/config:/app/config xzsk2/efb-wechat-docker:latest
```

### 登录

```bash
docker logs efb-wechat
```

### 停止

```bash
docker container stop efb-wechat
```
