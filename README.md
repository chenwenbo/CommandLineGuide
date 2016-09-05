# CommandLineGuide
整理一些命令行下的常用命令，很多命令是zsh的特性，持续添加一些实用的命令

## 命令行跳转

* ctrl + p : 显示前一条命令
* ctrl + n : 显示后一条命令
* ctrl + a : 跳转到行首
* ctrl + e : 跳转到行尾
* ctrl + u : 取消当前命令的输入
* ctrl + k : 清除光标之后的命令
* ctrl + c : 中断命令的执行
* ctrl + d : 向前删
* ctrl + h : 向后删
* ctrl + b : 向后跳转
* ctrl + f : 向前跳转
* alt + b : 以单词为单位向后跳转
* alt + f : 以单词为单位向前跳转
* alt + r : 查找历史命令
* alt + d : 以单词为单位删除。
* cd : 进入用户主目录
* cd - : 进入上个目录
* pushd : 压栈
* popd : 读取栈顶元素

## 常用命令

### 基本命令

* ctrl + w : 以单词为单位向后删除字符
* alt + d : 以单词为单位向前删除字符
* alt + . : 拿到上一条命令的内容
* pgrep -l + name : 查找进程pid
* sudo + command : 以超级管理员身份执行
* netstat -tln | grep 8080 : 查看端口占用情况
* ps -ef :查看进行是否运行
* ps -aux : 查看进程
* kill -9 + pid:终止进程
* sort : 排序
* alias : 查看系统中所有的alias
* ps : 查看进程
* grep : 查询字符（可用ack替换）
* man : 查看当前命令帮助文档
* shutdown : 关机
* chmod : 改变文件权限
* touch : 创建一个空文件
* take : 创建目录并切换到该目录
* tree : 以树的方式列出当前目录的递归结构
* ack : 字符查找 ack str
* top : 查看系统进行情况 linux / mac os 上可以用htop更加直观
* tee : 既能重定向到文件中，也能在终端中看到效果 eg : echo hello | tee test.log
* rm -rf : 忽略提示递归删除，多用于目录删除
* mv : 移动文件、重命名文件
* mv -r : 移动文件夹
* ls -a : 查看所有文件，包含隐藏文件
* history : 查看历史命令记录
* date : 显示时间
* cal : 显示日历
* bc : 计算器
* ZZ : 类似为vim中:wq
* r foo=bar : 将前一条命令的字符进行替换

### 显示文件

* cat : 从第一行开始显示文件内容
* tac : 从最后一行开始显示文件内容
* more : 一页一页显示文件内容  enter:向下反一行 space:向下翻一页 /str:搜索 q:离开 b:向回翻
* less : 与more类型，但是可以向前翻页，pageup / pagedown
* head : 只看头几行
* tail : 只看尾几行
* tail -f : 动态显示文件内容

### 压缩 解压缩
* zip : 压缩
* unzip : 解压缩
* tar : 压缩/解压缩

### grep命令详解

* find / -name filename.txt根据名称查找/目录下的filename.txt文件。
* find . -name "*.xml"递归查找所有的xml文件。
* find . -name "*.xml" |xargs grep "hello world"递归查找所有文件内容中包含hello world的xml文件。
* grep -H 'spring' *.xml查找所以有的包含spring的xml文件。
* find ./ -size 0 | xargs rm -f &删除文件大小为零的文件。
* ls -l | grep '.jar'查找当前目录中的所有jar文件。
* grep 'test' d*显示所有以d开头的文件中包含test的行。
* grep 'test' aa bb cc显示在aa，bb，cc文件中匹配test的行。
* grep '[a-z]\{5\}' aa显示所有包含每个字符串至少有5个连续小写字符的字符串的行。

### ps

ps -aux 是以BSD方式显示

* a 显示所有用户的进程(show processes for all users)
* u 显示用户(display the process's user/owner)
* x 显示无控制终端的进程(also show processes not attached to a terminal)

ps -ef 是以System V方式显示，该种方式比BSD方式显示的多

* e 显示所有用户的进程(all processes)此参数的效果和指定"a"参数相同
* f  用ASCII字符显示树状结构，表达程序间的相互关系(ASCII art forest)

### 重定向
* > ：已覆盖的方式，把命令的正确输出输出到指定的文件或者设备中
* >> : 已追加的方式，把命令的正确输出输出到指定的文件或者设备中
* < : 输入重定向，以文件或者设备中的内容作为输入 
* << : 输入重定向，以文件或者设备中的内容作为输入(追加) 
