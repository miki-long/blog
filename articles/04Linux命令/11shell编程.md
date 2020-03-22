1. 查看 系统 shell 版本
```
    cat /etc/Shells
```    
2. 使用 zsh 编写校本 新建 HelloWorld.sh 并且内容为：
```
    #!/bin/zsh
    #this line is a comment
    echo "hello world"
    

    #！ //程序开头
    /bin/zsh //使用的zsh 的解析器的具体位置
```    
3. 执行脚本
```    
    zsh HelloWorld.sh //输出
```    
4. 给脚本加上可执行权限
```
    chmod +x HelloWorld.sh
    ./HelloWorld.sh //输出
```    
5. 添加到全局环境
```
    mv HelloWorld.sh /usr/local/bin
    HelloWorld.sh //输出
```    
6. 输出校本运行情况（打日志）
```    
    zsh -x a.sh
```
7. 判断一个命令是否是內建命令
> 內建命令是指bash 自带命令，不需要在环境变量中的命令
```
    type cd
```   
8. 查看指令别名
```
     alias
```     
9. 在当前环境中自定义别名，只在当前shell 中起作用
```
    alias long='ls -la'
```    
10. 删除别名
```
    unalias long
```
11. 永久的alias 请看 zsh 中实现alias


12. 