## 1、使用 openssl 生成自定义证书


### 生成 server.key
> 在nginx 配置目录输入下面命令，可以看到目录下，多了一个server.key文件，接下来输入两次密码

    openssl genrsa -des3 -out server.key 2048
    
### 去除输入密码步骤

    openssl rsa -in server.key -out server.key
    
### 创建服务器证书的申请文件 server.csr

> country name 填 CN Common Name 填需要指定https 访问的域名

    openssl req -new -key server.key -out server.csr
    
### 创建ca 证书

    openssl req -new -x509 -key server.key -out ca.crt -days 3650

### 创建为期十年的服务器证书

    openssl x509 -req -days 3650 -in server.csr -CA ca.crt -CAkey server.key -CAcreateserial -out server.crt
    
> 到这个时候我们文件夹里面一共创建了 5 个证书 server.key、server.csr、ca.crt、server.crt、ca.srl，

### 配置nginx

    ssl_certificate     ./server.crt;#配置证书位置
    ssl_certificate_key  ./server.key;#配置秘钥位置
    #ssl_client_certificate ca.crt;#双向认证
    #ssl_verify_client on; #双向认证
    


