### shadowsocks-manager服务端一键部署脚本

本脚本纯属学习用，请勿用于商业活动


### 安装方法

安装wget
```
# centos
yum -y install wget

# Ubuntu
apt-get -y istall wget
```

安装服务
```
rm -rf ./install.sh ./shadowsocks-manager.log
wget --no-check-certificate https://raw.githubusercontent.com/quniu/ssmgr-deploy/master/install.sh
chmod +x install.sh
./install.sh 2>&1 | tee shadowsocks-manager.log
```

### 安装说明
日志在`/root/`下面

脚本在`/root/`下面

shadowsocks-manager 安装目录在`/usr/local/`下面



### shadowsocks-manager版本

服务端安装的是shadowsocks-manager最新打包版本

具体shadowsocks-manager版本 [查看releases最新版](https://github.com/quniu/shadowsocks-manager/releases)



### 端口说明
python版本启用`6000`端口

libev版本启用`6001`端口

manager端启用`6002`端口



### 查看shadowsocksr服务

默认安装成功之后会自动启动服务

python版本
```
service shadowsocks-manager-python status
service shadowsocks-manager-python stop
service shadowsocks-manager-python start
```

libev版本
```
service shadowsocks-manager-libev status
service shadowsocks-manager-libev stop
service shadowsocks-manager-libev start
```
