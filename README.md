## deepin常用软件安装

* 1 remmina : `sudo apt install remmina-plugin-spice`

* 2 [snpad安装](https://blog.csdn.net/u010318957/article/details/115204096)

* 3 goland,phpstorm: deepin store

* 4 github ssh: `ssh-keygen -t rsa -b 4096  -C "hammercui@163.com"` 

### 5 nodejs 环境

淘宝镜像
```
npm config set registry https://registry.npm.taobao.org
```

安装nrm，切换代理
```

sudo npm install nrm -g  --registry https://registry.npm.taobao.org
```

安装n，切换node版本
```
sudo npm install n -g
```

### 6 go环境配置
vim ~/.bashrc
```
# go path
export GOPATH=/home/hammer/Desktop/goPath 
# go proxy
export GOPROXY=https://goproxy.cn,direct
# go bin
export GOBIN=$GOPATH/bin
export PATH=$PATH:$GOROOT/bin
export PATH=$PATH:$GOPATH/bin
```

```
source ~/.bashrc
```

### 7 goland快捷键

常用插件：

* vistual studio keymap

* Material Theme UI

* 无限试用：Plugins添加第三方插件地址`https://plugins.zhile.io/,搜索`IDE Eval Reset`安装


快捷键配置：

* 前进/Forward: control+=
* 后退/Back： control+-
* 全文搜索Find in Path： shift+alt+f
* 全文替换Replace in Path： shift+alt+h
* 文件搜索Find：control+f
* 文件替换Replace: control+h
* 文件结构Fille Structure: control+F12
* 搜索文件Search Every: control+T

### 8 qv2ray 
>代理

1. 下载https://github.com/Qv2ray/Qv2ray/releases

2. 下载v2ray-core  https://github.com/v2fly/v2ray-core/releases

3. 配置v2ray-core,内核设置https://qv2ray.net/getting-started/step2.html#download-v2ray-core-files
3.1 v2ray核心可执行文件路径：/home/hammer/Downloads/v2ray-linux-64/v2ray
3.2 v2ray资源目录：/home/hammer/Downloads/v2ray-linux-64

4. 设置订阅

新建分组->订阅设置->订阅类型(base64)

### 8 安装win7虚拟机

1.官网下载virtual box 6.1
2.下载win7镜像msdn

### 9 系统自带Android虚拟机

1.打开设置页面`/usr/bin/uengine-launch.sh --package=org.anbox.appmgr --component=org.anbox.appmgr.AppViewActivity`
2. 安装软件`apt search uengine ihunman`
3. 安装 `sudo apt install uengine.com.tencent.mobileqq`


### 10 安装dotnet
>.net 6是大一统的版本

debian10


```
wget https://packages.microsoft.com/config/debian/10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
rm packages-microsoft-prod.deb
```

```
sudo apt-get update; \
  sudo apt-get install -y apt-transport-https && \
  sudo apt-get update && \
  sudo apt-get install -y dotnet-sdk-6.0
```

### 11 安装git-lfs

```
curl -o /etc/apt/sources.list.d/git-lfs.list "https://packagecloud.io/install/repositories/github/git-lfs/config_file.list?os=debian&dist=stretch&source=script"
curl -L "https://packagecloud.io/github/git-lfs/gpgkey" 2> /dev/null | apt-key add -
apt update && apt install git-lfs
```