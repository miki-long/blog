1、安装 在以下地址下载安装包

    http://nginx.org/en/download.html 
    
2、解压 nginx-xx 包

3、安装

    ./configure
    sudo make
    sudo make install
    
4、文件目录

    /usr/local/bin/nginx //启动文件
    /usr/local/etc/nginx/nginx.conf //配置文件

5、启动

    sudo /usr/local/bin/nginx
    
6、设置全局变量

    sudo ln -s /usr/local/bin/nginx  /usr/local/bin/nginx
    
    //设置nginx 的快捷方式
    
7、全局任意地方使用

    sudo nginx