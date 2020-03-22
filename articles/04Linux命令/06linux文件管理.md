### 文件与目录相关指令

指令 | 详情
--- | ---
 touch test.js | 创建test.js 文件
 rm test.js | 删除 test.js 文件
 pwd | 查看当前目录的完整目录
 mv test.js /Users/mickey/Desktop | 把 test.js 移动到 /Users/mickey/Desktop 该路径
mv test.js test.css | 把 test.js 修改为 test.css
cat test.js | 查看test.js 文件
head -n 30  access.log-2017-12-12 | 查看 access.log-2017-12-12 前 30 行
tail -n 30  access.log-2017-12-12 | 查看 access.log-2017-12-12 前 30 行
mkdir test | 创建 test 目录
rmdir test | 删除 test 空目录
rm -r test | 删除 test 目录
cp a.test /Users/mickey/Desktop/testa | 复制a.test 文件 到 /Users/mickey/Desktop/testa 目录
cp a.test b.test | 把 a.test 复制为 b.test
cp * ../b | 把当前目录所有 复制到上一层目录的b 目录下
ls -la | 参数 -l 表示列出每个文件的详细信息，-a 表示列出所有文件，包括隐藏文件 
gzip install.log | 压缩 install.log 为 install.log.gz（压缩单个文件）
gunzip install.log.gz | 解压 install.log.gz 为 install.log
bzip2 install.log | 把install.log 文件压缩为 install.log.bz2 文件
 bzip2 -d install.log.bz2 | 把  install.log.bz2 解压 为 install.log
tar -zcvf testa.tgz ./testa | 把 testa 目录 压缩成为 testa.tgz（可以压缩目录）
tar -zxvf testa.tgz | 把 testa.tgz 解压为 tasta

### zcvf 解释

字母 | 意义
--- | ---
z | 使用 gzip 压缩
c | 创建压缩文件 
v | 显示当前被压缩的文件
f | 使用文件名 testa.tgz

