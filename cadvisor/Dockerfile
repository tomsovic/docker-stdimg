FROM google/cadvisor:v0.26.1
LABEL maintainer="xdxiaozhong@gmail.com"
RUN apk update && \
    apk --no-cache add tzdata && \
    cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone && \
    apk del tzdata && \
    rm -rf /var/cache/apk/*
