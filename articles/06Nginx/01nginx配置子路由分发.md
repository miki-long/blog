
nginx

```
location /extend/ {
    proxy_pass http://enweb-extend-dev.test.seewo.com/;
    proxy_redirect              off;
    
    proxy_set_header                X-Forwarded-Url         "$scheme://$host$request_uri";
    proxy_http_version  1.1;
    proxy_set_header    Connection "";
    proxy_set_header    Cookie $http_cookie;
    proxy_set_header    Host enweb-extend-dev.test.seewo.com;
    proxy_set_header    x_ccloud_pre 1;
    proxy_set_header            Host $host;
    proxy_set_header            X-Real-IP $remote_addr;
    proxy_set_header            X-Forwarded-For $proxy_add_x_forwarded_for;
    allow all;
  }
```


host

```
10.10.14.186 enweb-extend-dev.test.seewo.com
```