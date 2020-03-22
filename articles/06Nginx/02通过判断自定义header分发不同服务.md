```
upstream  teacher-web{
        server 127.0.0.1:13801 weight=1 fail_timeout=20s;        
        keepalive 16;
}

upstream  teacher-web-new{
        server 127.0.0.1:13800 weight=1 fail_timeout=20s;        
        keepalive 16;
}

server {
    listen       80;
    listen       443 ssl;
    ssl_certificate     /usr/local/etc/nginx/https/seewo.com.crt;#配置证书位置
    ssl_certificate_key  /usr/local/etc/nginx/https/seewo.com.key;#配置秘钥位置
    # add_header X-Frame-Options ALLOW-FROM;
    server_name  teacher.seewo.com;

    location / {

            // ....

            if ($http_x_app_type = 'newApp') {
              proxy_pass http://teacher-web-new;
              break;
            }
            proxy_pass http://teacher-web;
    }
}

```