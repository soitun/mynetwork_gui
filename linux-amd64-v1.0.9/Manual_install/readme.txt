安装说明
一、程序文件安装
1、将mynetwork-linux-amd64 复制到 /usr/local/bin

cp ./mynetwork-linux-amd64 /usr/local/bin/mynetwork
chmod +x /usr/local/bin

2、测试
终端直接运行下面的命令， 如果正常，会打印帮助信息。
mynetwork 

3、初始化节点 (仅需运行一次)
mynetwork init

二、安装 systemd 服务

1、将 mynetwork.service 复制到 systemd 目录

cp ./mynetwork.service  /lib/systemd/system/

2、启动服务

systemctl daemon-reload
systemctl start mynetwork.service

3、检查服务状态

systemctl status mynetwork.service

三、关联节点归属

将节点关联到您的名下，所有您名下的节点会自动组网：

mynetwork bind

用微信扫描屏幕上的二维码， 再常按手机上的二维码，点击弹出菜单中的 [ 前往图中包含的小程序 ]， 根据提示完成授权


四、说明

新节点注册成功后，会有大概3分钟左右，会自动同步组网。
