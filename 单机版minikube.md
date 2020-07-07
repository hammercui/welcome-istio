<!--
 * @Author: hammercui
 * @Date: 2020-07-07 17:14:50
 * @LastEditors: hammercui
 * @LastEditTime: 2020-07-07 20:53:42
 * @FilePath: /wel-istio/单机版minikube.md
 * @Description: 描述
--> 
# 单机版开发环境使用minikube

### 环境安装
阿里云安装minikube

```
curl -Lo minikube http://kubernetes.oss-cn-hangzhou.aliyuncs.com/minikube/releases/v1.11.0/minikube-linux-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/
```
安装conntrack

```
sudo apt-get install -y conntrack
```

查看minikube版本 

`minikube version`

启动Minikube(在root用户下执行)

```
#使用虚拟机启动
minikube start --vm-driver=virtualbox
#直接使用linux启动
minikube start --vm-driver=none
```

### 安装插件

### 其他管理命令

```
#启停集群
minikube start/stop 
 
#删除集群
minikube delete
rm -rf ~/.minikube
kubeadm reset
 
#查看当前集群插件状态
minikube addons list
#打开某个插件（minikube必须在运行状态）
minikube addons enable heapster
minikube addons enable dashboard
#查看minikub的IP地址
minikube ip
#查看minikube安装状态
minikube status
# 查看节点信息
kubectl get nodes 


```

### FAQ

#### 1.  The "docker" driver should not be used with root privileges.

建议使用minikube start --vm-driver=none模式启动


