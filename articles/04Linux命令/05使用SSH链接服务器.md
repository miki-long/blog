> 根据ssh 链接服务器，可以避免每次都输入账号密码登录服务器，而且能防止密码泄露

### ssh 认证流程


1. 生成密钥
```
    ssh-keygen
```    
2. 找出密钥地址

    
3. 把公钥复制到服务器列表中

> 链接服务器，打开/home/mickey/.ssh ， vim authorized_keys 在后面追加key

1. SSH远程链接Linux服务器
```
    ssh student@127.0.0.1 -p 2222 -i ~/.ssh/MyLinux
```    
> student 为服务器的用户名,-p后面接端口名称，-i 后面公钥地址

