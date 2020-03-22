### 一、Mac 下安装 Apache

1. mac 自带 Apache 只需要打开 Apache 即可

```
sudo apachectl start
```

2. 在浏览器输入,看到 It works! 返回
  
```
http://localhost
```

3. 修改配置文件
  
```
sudo vi /etc/apache2/httpd.conf
```

> 把下面这行反注释

```
#Include /private/etc/apache2/extra/httpd-vhosts.conf
```

4. 重启 Apache
  
```
sudo apachectl restart
```

5. 新增配置

```
sudo vi /etc/apache2/extra/httpd-vhosts.conf
```

> 在文件后面新增

```
<VirtualHost *:80>
    DocumentRoot "/Library/WebServer/Documents"
    ServerName localhost
    ErrorLog "/private/var/log/apache2/localhost-error_log"
    CustomLog "/private/var/log/apache2/localhost-access_log" common
</VirtualHost>
 
<VirtualHost *:80>
    DocumentRoot "/Users/snandy/work"
    ServerName mysites
    ErrorLog "/private/var/log/apache2/sites-error_log"
    CustomLog "/private/var/log/apache2/sites-access_log" common
<Directory />
            Options Indexes FollowSymLinks MultiViews
            AllowOverride None
            Order deny,allow
            Allow from all
  </Directory>
</VirtualHost>
```

6. 重启 Apache
  
```
sudo apachectl restart
```

7. 停止 Apache
  
```
sudo apachectl stop
```

### 二、使用 Apache test 进行 get 请求

```
ab -n 100 -c 10 https://www.baidu.com/
```

### 三、ab 命令行参数说明





