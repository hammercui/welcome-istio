# centos安装k8s

### 安装docker
```cassandraql
// 安装docker
$ yum install -y docker-ce
// 开机启动 && 启动服务
$ systemctl enable docker && systemctl start docker
```

### 安装k8s
```cassandraql
# 在/etc/yum.repos.d 下创建k8s.repos, 并添加如下内容

name=Kubernetes
baseurl=http://mirrors.aliyun.com/kubernetes/yum/repos/kubernetes-el7-x86_64
enabled=1
gpgcheck=0
repo_gpgcheck=0
gpgkey=http://mirrors.aliyun.com/kubernetes/yum/doc/yum-key.gpg
       http://mirrors.aliyun.com/kubernetes/yum/doc/rpm-package-key.gpg
```

安装
```cassandraql
// 安装
yum install -y kubelet kubeadm kubectl
systemctl enable kubelet  && systemctl start kubelet
```