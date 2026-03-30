FROM amazoncorretto:21-alpine

LABEL maintainer="docker@visualticket.cn"

RUN apk add --no-cache \
    font-noto \
    font-noto-cjk \
    fontconfig \
    && ln -sf /usr/share/zoneinfo/$TZ /etc/localtime \
    && echo $TZ > /etc/timezone

ENV TZ=Asia/Shanghai
ENV LANG=C.UTF-8