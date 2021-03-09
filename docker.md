- 安装
  ```bash
  # UOS安装docker
  sudo apt install docker.io
  ```
- 将当前登录用户加入docker用户组
  ```bash
  sudo gpasswd -a $USER docker
  newgrp docker
  service docker restart
  ```
- 添加国内镜像仓库
  ```bash
  vim /etc/docker/daemon.json
  ```
  ```json
  // 添加以下内容
  {
    "registry-mirrors": [
    "http://hub-mirror.c.163.com",
    "https://registry.docker-cn.com",
    "https://docker.mirrors.ustc.edu.cn"
    ],
    "dns": ["8.8.8.8","8.8.4.4"]
  }
  ```
  ```bash
  sudo systemctl daemon-reload
  sudo service docker restart
  ```

- docker安装mongodb
  ```bash
  docker pull mongo:latest

  docker run -itd --name mongo -p 27017:27017 -v ~/mongodb:/data/db mongo --auth

  docker exec -it mongo mongo admin

  # authorization configure
  db.createUser({ user:'admin',pwd:'654321',roles:[ { role:'userAdminAnyDatabase', db: 'admin'}]});
  db.auth("admin", "654321")
  db.grantRolesToUser("admin", [ { role: "readWrite", db: "crawler" } ])
  db.grantRolesToUser("admin", [ { role: "readWrite", db: "crawler_statistic" } ])
  ```
- docker安装mariadb
  ```bash
  docker pull mariadb
  docker run --name mariadb -p 3306:3306 -e MYSQL_ROOT_PASSWORD=your_root_password -v /data/mariadb/data:/var/lib/mysql -d mariadb
  docker ps -a
  docker exec -it your_mariadb_container_id bash
  mysql -uroot -pxxx
  ```

- docker安装redis
  ```bash
  # 拉取镜像
  docker pull redis:3.2
  # 启动容器
  docker run -p 6379:6379 --name myredis -v /root/docker_redis/data:/data -d redis:3.2 redis-server --appendonly yes --requirepass your_password
  ```