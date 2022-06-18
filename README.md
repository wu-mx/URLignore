# URLignore
[中文文档](./README-zh.md)
A simple node widget that supports removing duplicate configuration nodes, adding countries and add custom content automatically.<br>
Supports SS/SSR/Vmess/Trojan/Https.

## Quick Start
### 1.Install Node.js and NPM.
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

### 2.Prepare the node file and place a node link per line and rename it to url.<br>

### 3.Clone the repository and install NPM libraries：
````shell
git clone https://github.com/wu-mx/URLignore.git
cd ./URLignore
npm install
````

### 4.Copy the url file into the URLignore folder.<br>
### 5.Start URLignore:
```shell
npm run start
//Or node index
```
### 6.Wait a few seconds, URLignore will automatically complete the node processing and output the processed nodes to the out file.

## Configuration
URLignore now supports custom configuration.<br>
The custom configuration is located in config.js.<br>
The default configuration looks like this：
```javascript
module.exports={
    nodeAddName:'', //Text contents added after the node names.
    dnsServers:['8.8.8.8','1.1.1.1'] //The DNS servers used to resolve the domain when processing node countries are stored in array format. No modification is required unless necessary.
}
```
For example, when the configuration file looks like this：
```javascript
module.exports={
    nodeAddName:' | URLignore',
    dnsServers:['223.5.5.5','114.114.114.114']
}
```
The DNS servers 223.5.5.5 and 114.114.114.114 are used, and the output node name is followed by the " | URLignore" suffix, such as "🇭🇰HK 1 | URLignore".

### URLignore follows [GPLv3](./LICENSE).
