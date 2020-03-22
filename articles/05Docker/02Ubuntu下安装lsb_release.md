1. 现象
```
root@48a52763c490:/# lsb_release -a
bash: lsb_release: command not found
```
2. 方法
```
root@48a52763c490:/# yum install -y redhat-lsb
There are no enabled repos.
Run "yum repolist all" to see the repos you have.
You can enable repos with yum-config-manager --enable <repo>

// 尝试上面的使用yum 安装不允许

sudo apt install --reinstall base-files lsb-release lsb-base
// 到这里就可以了
```