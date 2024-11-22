FROM jenkins/jenkins:lts

# 切换到 root 用户
USER root

# 设置 root 用户密码
RUN echo 'root:root' | chpasswd

# 替换为阿里云的 Debian 镜像源
RUN echo "deb http://mirrors.aliyun.com/debian bookworm main contrib non-free" > /etc/apt/sources.list && \
    echo "deb http://mirrors.aliyun.com/debian bookworm-updates main contrib non-free" >> /etc/apt/sources.list && \
    echo "deb http://mirrors.aliyun.com/debian-security bookworm-security main contrib non-free" >> /etc/apt/sources.list

# 切换回 Jenkins 用户
USER jenkins
