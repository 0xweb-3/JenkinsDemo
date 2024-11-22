# JenkinsDemo
JenkinsDemo

# 查看密码
```angular2html
/var/jenkins_home/secrets/initialAdminPassword
```

# 在内部安装docker
```angular2html
# 使用 JenkinsDocker/docker-compose.yml

docker-compose build 
docker-compose up -d

# 进入到容器中
docker exec -it jenkinsDocker /bin/bash

su - #root
apt-get update
apt-get install docker.io

groupadd -g 999 docker
usermod -aG docker jenkins
```