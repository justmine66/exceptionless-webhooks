一个 Exceptionless 相关 WebHooks 项目。

# 目的
当Exceptionless触发配置的WebHooks通知类型时，如Error、LogError，发送消息到 DingTalk（钉钉），以便实时知道线上程序运行情况。

# 部署
## docker
docker run -d -p 8000:80 justmine/exceptionless.api.webhook:0.0.0

## kubernetes（推荐）

[deployment.yml](https://github.com/justmine66/exceptionless-webhooks/blob/master/k8s/web.yml)

# 配置

请先部署好webhook钩子。

## Exceptionless

Admin => Projects => Integrations => Add Web Hook：

![Image text](https://github.com/justmine66/exceptionless-webhooks/blob/master/config.png)

# 效果图

![Image text](https://github.com/justmine66/exceptionless-webhooks/blob/master/result.png)

# changes

1. 添加容器化部署脚本，支持docker、kubernetes。
2. 扩展事件模型，添加环境、来源等信息。
3. 升级项目为netcoreapp2.1。
4. 优化httpclient使用方式。
5. 添加事件时间本地化设置。
