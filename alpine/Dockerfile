FROM alpine:3.6
# Use USTC mirror
RUN echo http://mirrors.ustc.edu.cn/alpine/v3.6/main > /etc/apk/repositories && \
    echo http://mirrors.ustc.edu.cn/alpine/v3.6/community >> /etc/apk/repositories
# Configure localtime and timezone
RUN apk update && \
    apk --no-cache add tzdata && \
    cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone && \
    apk del tzdata && \
    rm -rf /var/cache/apk/*
