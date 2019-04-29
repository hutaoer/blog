# linux 常用命令

## 查看内核版本命令
* `uname -a`
* `cat /proc/version`

## 查看Linux系统版本的命令
* `cat /etc/redhat-release`，这种方法只适合Redhat系的Linux
* `cat /etc/issue`，这个命令亲测，在`CentOS Linux release 7.2.1511`系统上，输出的文本为`Kernel \r on an \m`
* `lsb_release -a`，提示`lsb_release: command not found`，需要先安装: `yum install -y redhat-lsb`，再执行`lsb_release -a`