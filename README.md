# CommandLineGuide
整理一些命令行下的常用命令，持续添加一些实用的命令

## 命令行跳转

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

## 常用命令

### 基本命令

* date : 显示时间
* cal : 显示日历
* bc : 计算器
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
