#URLignore
一个简单的节点去重小工具，无需第三方Nodejs库，支持去重不同名但为同一配置的节点。<br>
支持SS/SSR/Vmess/Trojan。

##快速开始
###1.安装Node.js和npm
####Ubntu/Debian:
```shell
sudo apt-get update
sudo apt-get install nodejs
```

####Fedora/Centos/Redhat:
```shell
curl -sL https://rpm.nodesource.com/setup_16.x | bash -
sudo yum -y install nodejs
```

####2.准备好节点文件，一行一个节点链接，重命名为url。<br>

####3.克隆仓库：
````shell
git clone https://github.com/wu-mx/URLignore.git
````

####4.将url文件拷入URLignore文件夹<br>
####5.在命令行执行:
```shell
npm run start
```
####6.稍候片刻，URLignore将会自动完成节点去重，并将去重完毕的文件输出到目录下的out文件。
<br>
Licence:GPLv3
