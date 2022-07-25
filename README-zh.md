# URLignore
## 从2022年7月25日起，urlignore取消开源协议，现在只能进行查看源码、分叉。禁止使用和修改该项目。<br>如果你在你的项目中使用了urlignore，请立即移除。

一个简单的节点处理小工具，支持去重不同名但为同一配置的节点,可自动添加国家和自定义内容。<br>
支持SS/SSR/Vmess/Trojan/Https。

## 快速开始
### 1.安装Node.js和npm
#### Ubuntu/Debian:
```shell
sudo apt-get update
sudo apt-get install nodejs
```

#### Fedora/Centos/Redhat:
```shell
curl -sL https://rpm.nodesource.com/setup_16.x | bash -
sudo yum -y install nodejs
```

### 2.准备好节点文件，一行一个节点链接，重命名为url。<br>

### 3.克隆仓库并安装依赖：
````shell
git clone https://github.com/wu-mx/URLignore.git
cd ./URLignore
npm install
````

### 4.将url文件拷入URLignore文件夹<br>
### 5.在命令行执行:
```shell
npm run start
//或者 node index
```
### 6.稍候片刻，URLignore将会自动完成节点处理，并将处理完毕的文件输出到目录下的out文件。

## 配置文件
URLignore现已支持自定义配置。<br>
自定义配置位于config.js中，以json格式保存，并通过module.export导出。<br>
默认配置如下：
```javascript
module.exports={
    nodeAddName:'', //在节点后面添加的文字内容
    dnsServers:['8.8.8.8','1.1.1.1'] //处理节点国家时所使用的用于解析域名的DNS服务器，以数组格式保存。非必要无需修改。
}
```
示例，当配置文件如下时：
```javascript
module.exports={
    nodeAddName:' | URLignore',
    dnsServers:['223.5.5.5','114.114.114.114']
}
```
则使用223.5.5.5和114.114.114.114的DNS服务器，且在输出的节点名后会有" | URLignore"的后缀，如"🇭🇰HK 1 | URLignore"。
