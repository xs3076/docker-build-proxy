FROM amazoncorretto:21-alpine

LABEL maintainer="docker@visualticket.cn"

ENV TZ=Asia/Shanghai
ENV LANG=C.UTF-8

RUN apk add --no-cache \
        font-noto \
        font-noto-cjk \
        fontconfig \
        tzdata \
    && ln -sf /usr/share/zoneinfo/$TZ /etc/localtime \
    && echo $TZ > /etc/timezone
