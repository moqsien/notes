###  UOS（统信操作系统个人版）作为生产力工具

- ISO下载地址

  ```text
  https://www.chinauos.com/resource/download-personal
  ```
- 制作EFI启动U盘（Linux）
  ```bash
  # 查看U盘信息
  sudo fdisk -l
  # 格式化U盘，例如U盘为/dev/sda
  sudo fdisk /dev/sda
  # 查看fdisk命令的子命令菜单
  m
  # 烧录
  dd if=/path_to_iso/xxx.iso of=/dev/sda bs=2M
  ```
- 安装UOS
  ```text
  进BIOS修改启动项，U盘启动之后，如果报/live/vmlinuz not found error，则在安 安装的grub界面按下e，编辑/live/vmlinuz为/live/vmlinuz.efi，然后按照下方的提示进行保存，即可继续进入安装界面。
  分区看个人喜好，一般根目录/在25G以上较好，系统本身会占去7-8G，后面可能自己还要手动安装一些软件；/opt可以独立分区，并且稍微给大一点，因为UOS通过应用商店安装的软件都会放在/opt/app目录下，软件安装多，需要空间可能比较大，建议45G以上；swap，交换空间，内存16G以内的机器，可以分5-10G给交换空间；留出20G空间备用，防止某些分区需要扩容。其余看心情怎么分，像/usr/local、/var之类的要不要独立分区等；最后剩下的全给/home。
  ```
- 开启开发者模式
  ```text
  # 安装完成后第一次启动会让设置用户名和密码，这一点与其他发行版不同，与windows类似。
  到UOS官网注册账号，用账号密码登录，即可开启开发者模式。方便安装软件。
  ```
- 内核升级
  ```bash
  # 安装完成后，如果硬件较新，可能需要手动升级内核
  # https://kernel.ubuntu.com/~kernel-ppa/mainline/
  # 可以安装同是debian系的ubuntu的内核安装包；
  # 如果要偏流畅可以用lowlatency版，一般用generic版。可以尝试最新的稳定版。
  # 确认新内核正常启动，无问题之后，查询并删除旧的不想要的内核
  dpkg --get-selections | grep linux
  sudo apt-get remove linux-x.x.x-xxxx
  ```
- wifi网速慢问题解决
  ```bash
  sudo vim /etc/modprobe.d/iwlwifi.conf
  # 修改11n_disable=0和swcrypto=1，重启之后生效
  ```
- 应用软件列表
  - 办公类
    - wps
    - foxitreader([ubuntukylin](https://www.ubuntukylin.com/applications/21-cn.html))
    - dingtalk([ubuntukylin](https://www.ubuntukylin.com/applications/67-cn.html))
    - drawio([github](https://github.com/jgraph/drawio-desktop/releases))
    - typora
    - teamviewer([官网下载](https://www.teamviewer.cn/cn/download/previous-versions/))
  - 开发类
    - pycharm([官网下载](https://www.jetbrains.com/pycharm/download/#section=linux))
    - LiteIDE([github](https://github.com/visualfc/liteide/releases))
    - vscode([官网下载](https://code.visualstudio.com/))
    - kite engine([官网下载](https://www.kite.com/download/))
    - dbeaver([官网下载](https://dbeaver.io/download/))
    - robo3t([官网下载](https://robomongo.org/download))
    - Redis Desktop([github](https://github.com/qishibo/AnotherRedisDesktopManager/releases))
    - charles
    - wireshark
    - postman
    - diffuse
    - sublime text3
    - docker(sudo apt install docker.io)
  - 社交类
    - wechat
    - qq
  - 工具类
    - motrix([github](https://github.com/agalwood/Motrix/releases))
    - baidunetdisk(百度网盘)
    - shadowsocks([github](https://github.com/innoob/ss-qt5))
    - 360browser
    - appimage-installer([github](https://github.com/azubieta/appimage-installer/releases))
    - plank(sudo apt install plank)
    - hardinfo(sudo apt install hardinfo)
    - ulauncher([github](https://github.com/Ulauncher/Ulauncher/releases))
    - 360压缩
    - flameshot([github](https://github.com/flameshot-org/flameshot/releases))
    - gimp
    - krita
    - 华宇拼音输入法
    - calibre
  - 娱乐类
    - 网易运音乐
    - 腾讯视频
- 安装google-chrome
  ```bash
  wget -q -O - https://dl.google.com/linux/linux_signing_key.pub  | sudo apt-key add -
  sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
  sudo apt-get update
  sudo apt-get install google-chrome-stable
  sudo apt-get install freeglut3-dev
  pip install pyside2
  ```
- qt5安装
  ```bash
  sudo apt install build-essential
  sudo apt install gdb cmake
  sudo apt install libdtkwidget-dev qt5-default qtcreator
  ```
- 安装appImage格式包
  
  - 使用appimage-installer
- 安装二进制压缩包
  - 将包解压，mv到/opt下
  - 在/usr/share/applications/下创建图标描述文件，即可在菜单中看到应用软件启动图标
  ```text
  [Desktop Entry]
  Name=Pycharm
  Comment=Pycharm Community
  Exec=/opt/pycharm-community/bin/pycharm.sh
  Icon=/opt/pycharm-community/bin/pycharm.png
  Terminal=false
  Type=Application
  Encoding=UTF-8
  Categories=Development;
  Name[en_US]=Pycharm%   
  ```
  - 如果需要支持命令行启动，则创建软连接到/usr/bin/下

