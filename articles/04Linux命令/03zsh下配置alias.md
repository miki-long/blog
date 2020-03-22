1. 在 ~./.zshrc 中配置
```
    alias k56='ssh mickey@127.0.0.1'
```    
2. 运行生效
```
    source ~/.zshrc
```    
3. 查看是否是修改成功,找出修改点
```   
    alias
    //k56='ssh mickey@127.0.0.1'
```    
4. 确认
```
    ➜  ~ k56
    Last login: Sat Jan  6 10:18:23 2018 from 172.18.99.209
```