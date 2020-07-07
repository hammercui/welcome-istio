1 添加官方密钥
```
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
```
2 验证
```
sudo apt-key fingerprint 0EBFCD88
```

3 手动添加软件源
```
sudo vim /etc/apt/source.list 添加
deb [arch=amd64] https://download.docker.com/linux/debian stretch stable
```

4 更新
```
sudo apt-get update
```
5 查看可安装版本
```
apt-cache madison docker-ce
```
6 安装指定版本
```
sudo apt-get install docker-ce=5:19.03.11~3-0~debian-stretch docker-ce-cli=5:19.03.11~3-0~debian-stretch containerd.io
```
7 直接安装
```
sudo apt-get install docker-ce docker-ce-cli containerd.io
```