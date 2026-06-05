# 使用 RabbitMQ 官方基础镜像
FROM rabbitmq:3.12.14-management-alpine

# 设置维护者信息
LABEL maintainer="docer@visualticket.cn"

# 下载并安装延迟插件
RUN apk add --no-cache curl unzip \
    && curl -Lo /opt/rabbitmq_delayed_message_exchange-3.12.1.ez https://github.com/rabbitmq/rabbitmq-delayed-message-exchange/releases/download/v3.12.0/rabbitmq_delayed_message_exchange-3.12.0.ez\
    && mv /opt/rabbitmq_delayed_message_exchange-3.12.1.ez /plugins/ \
    && rabbitmq-plugins enable --offline rabbitmq_delayed_message_exchange \
    && apk del curl unzip

# 暴露端口
EXPOSE 5672 15672

# 定义环境变量
ENV RABBITMQ_DEFAULT_USER=user
ENV RABBITMQ_DEFAULT_PASS=password

# 启动 RabbitMQ 服务
CMD ["rabbitmq-server"]