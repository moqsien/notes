- 安装
  ```bash
  sudo apt install docker.io
  ```
- 将当前登录用户加入docker用户组
  ```bash
  sudo gpasswd -a $USER docker
  newgrp docker
  service docker restart
  ```
- docker安装mongodb
- docker安装mariadb
- docker安装redis