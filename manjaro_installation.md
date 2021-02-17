### How To Install Manjaro Linux On Your Machine

- download ISO images

  - https://mirrors.ustc.edu.cn/manjaro-cd/
  - https://manjaro.org.cn/category/download-manjaro

- format a USB DISK

  - check disk info

    ```bash
    sudo fdisk -l

    Disk /dev/sda：7.53 GiB，8086618112 字节，15794176 个扇区
    磁盘型号：USB DISK
    单元：扇区 / 1 * 512 = 512 字节
    扇区大小(逻辑/物理)：512 字节 / 512 字节
    I/O 大小(最小/最佳)：512 字节 / 512 字节
    磁盘标签类型：dos
    磁盘标识符：0x6732b8e4

    设备       启动    起点    末尾    扇区   大小 Id 类型
    /dev/sda1  *          0 5086847 5086848   2.4G  0 空
    /dev/sda2       5086848 5425343  338496 165.3M  1 FAT12
    ```

  - delete and create partions

    ```bash
    sudo fdisk /dev/sda
    m
    d
    d
    n
    ```

  - burn ISO images
    ```bash
    sudo dd if=manjaro_xfce.iso of=/dev/sda bs=2M
    ```
