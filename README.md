## 一、内容简介

1.    `LANMP` 指的是 `Linux` + `Apache` + `Nginx` + `MySQL` + `PHP` 运行环境。
2.	`LANMP` 一键安装包是用 `Linux Shell` 语言编写的，用于在 `Linux` 系统(`Redhat`/`CentOS`/`Debian`/`Ubuntu`)上一键安装 `LANMP`环境的工具包。

## 二、特点与优势

1.	3种Web环境自由组合

	`lnmp`、`lamp`、`lanmp`（Nginx前端Apache后端）可自主选择，甚至安装完后还可以自由调整。

2.	最新版本软件包

	全部采用最新稳定版本的软件包，如`PHP 5.4`（可选择`PHP 5.2`）系列，`MySQL 5.5`系列。

3.	下载更智能更方便

	自动从官方地址下载最新稳定版本源码安装，如果官网挂了或被和谐了，可自动从备选地址下载最新版。

4.	完美多用户支持

	配套了虚拟主机用户添加和删除脚本，因此可用来做虚拟主机销售。（主网站位于`/var/www`目录，用户网站位于`/home/user1`、`/home/user2`...）

5.	完善的扩展支持

	除小型依赖库外，都尽可能从源码编译安装。如PHP支持了`gd`,`memcache`,`xcache`,`pdo mysql`等扩展。

6.	多种PHP处理方式

	`Nginx`以`FastCGI`方式解析`PHP`，`Nginx`+`Apache`可选以`php moudle`或`FastCGI`方式方式解析`PHP`。

7.	模块化安装流程

	模块化、清晰的安装流程，脚本非常易于理解，因此您可以很容易修改脚本。

8.	简洁与高效

	只安装必须的东西，没有臃肿的图形界面。

9.	支持自动升级

	安装前可自动安装最新版本，安装后也可升级到最新版本。

10.	其他

	如`phpMyAdmin`支持额外的链接表特性，支持添加二级子域名，自定义`Rewrite`规则等等。

## 三、安装和使用

详细安装和使用说明请参阅 [《Wiki 文档》](https://github.com/wangyan/lanmp/wiki)

1、安装方法

稳定版是相对稳定的版本，开发版是更新频率较高的版本，带有新特性，但可能存在较多Bug。

方法一：直接下载已打包版本

	yum -y install screen  #Redhat/CentOS
	apt-get -y install screen  #Debian/Ubuntu
	screen -S lanmp
	wget -c http://wangyan.org/download/lanmp/lanmp-latest.tar.gz #安装稳定版
	wget -c http://wangyan.org/download/lanmp/lanmp-dev-latest.tar.gz #开发版（二选一）
	tar -zxf lanmp-*.tar.gz 
	cd lanmp && ./install.sh

方法二：通过Git下载（推荐）

	yum -y install screen git  #Redhat/CentOS
	apt-get -y install screen git-core git-gui  #Debian/Ubuntu
	screen -S lanmp
	git clone https://github.com/wangyan/lanmp.git
	cd lanmp && ./install.sh #安装稳定版
	cd lanmp && git checkout develop && ./install.sh #安装开发版（二选一）

3、虚拟主机管理

	cd lanmp/
	./vhost_add.sh #添加
	./vhost_del.sh #删除

4、自动升级

	cd lanmp/
	./upgrade.sh

## 四、注意事项

1.	可能会经常更新

	改进措施：日常更新会推送到`develop`分支，较稳定版本才推送到`master`主分支。

2.	可能会不兼容你的VPS

	改进措施：如果您安装失败，麻烦您将安装目录下的`log.txt`日志文件发给我分析 [WangYan@188.com](WangYan@188.com)

3.	针对512M内存的VPS进行了优化

	如果你的内存较低或更高，建议您要修改php或apache的配置文件。

## 五、联系方式

> Email: [WangYan#188.com](WangYan#188.com) （推荐）  
> Gtalk: [myidwy#gmail.com](myidwy#gmail.com)  
> Q Q群：[138082163](http://qun.qq.com/#jointhegroup/gid/138082163)  
> Twitter：[@wang_yan](https://twitter.com/wang_yan)  
> Home Page: [WangYan Blog](http://wangyan.org/blog)  
