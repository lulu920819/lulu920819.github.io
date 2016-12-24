---
title: ubuntu-app
categories: guide
date: 2016-12-24 16:37:44
tags:
- ubuntu
- ftp
---

# ubuntu + ftp

```
sudo apt-get update
sudo apt-get install vsftpd


sudo service vsftpd restart

```


```
新建"/home/uftp"目录作为用户主目录

打开"终端窗口"，输入"sudo mkdir /home/uftp"-->回车-->输入"sudo ls /home"-->回车-->有一个uftp目录，目录新建成功。
```

```
打开"终端窗口"，输入"sudo useradd -d /home/uftp -s /bin/bash uftp"-->回车-->用户新建成功-->输入"sudo passwd uftp"设置uftp用户的密码-->回车-->输入两次密码-->回车-->密码设置成功。

```


```
使用gedit修改配置文件/etc/vsftpd.conf

打开"终端窗口"，输入"sudo gedit /etc/vsftpd.conf"-->回车-->打开了vsftpd.conf文件，向文件中添加"userlist_deny=NO

userlist_enable=YES userlist_file=/etc/allowed_users"和"seccomp_sandbox=NO"-->使文件中的"local_enable=YES"-->保存。

```


```
使用gedit新建/etc/allowed_users文件

打开"终端窗口"，输入"sudo gedit /etc/allowed_users"-->回车-->输入uftp-->保存， 文件创建成功。

```


```
使用gedit查看/etc/ftpusers文件中的内容

打开"终端窗口"，输入"sudo gedit /etc/ftpusers"-->回车-->打开这个文件后，看一看有没有uftp这个用户名，如果没有，就直接退出。如果有就删除uftp,因为这个文件中记录的是不能访问FTP服务器的用户清单。

```


# xclip
copy the content of a file into the clipboard 

```
sudo apt-get install xclip
xclip -sel clip < ~/.ssh/id_ras.pub
```


# shutter
截图
	
	sudo apt-get install shutter


# diodon

剪贴板

	sudo apt-add-repository ppa:diodon-team/stable
	sudo apt-get update
	sudo apt-get install diodon
	# and for all Unity users there is also a scope
	sudo apt-get install unity-scope-diodon

# xmind
思维导图

	XMind（思维导图）
	官方下载：http://www.xmind.net/download/linux/
	chmod +x setup.sh
	sudo ./setup.sh
	cd  XMind_i386/ 
	双击XMIND


# todo
真的要解决，可以看代码github
	git clone git://github.com/keithfancher/Todo-Indicator.git
	python setup.py
	# maybe need
	sudo apt-get install --reinstall python-gi
	sudo apt-get install python-gi
	pip install pyinotify
	python-gi

	export PYTHONPATH = "PYTHONPATH:/usr/lib/python2.7/dist-packages"
	# run


# STICKYNOTES
便签
	sudo add-apt-repository ppa:umang/indicator-stickynotes

	sudo apt-get update

	sudo apt-get install indicator-stickynotes

# mendelay
	paper management software

[download](https://www.mendeley.com/newsfeed/)


# vim

[reference](https://github.com/ma6174/vim)

# sogou

[reference](http://pinyin.sogou.com/linux/?r=pinyin%E3%80%82)
	remember to log out


# cmatrix
	sudo apt-get install cmatrix
	cmatrix


# guake terminal
	sudo apt-get install guake
[reference](https://github.com/Guake/guake)

# tweak tools
change the desktop
	sudo add-apt-repository ppa:freyja-dev/unity-tweak-tool-daily
	sudo apt-get update
	duso apt-get install unity-tweak-tool

# guake
	sudo add-apt-repository ppa:webupd8team/unstable
	sudo apt-get update

# 下载
	http://jingyan.baidu.com/article/a65957f4e9adcf24e67f9bc0.html?st=2&net_type=&bd_page_type=1&os=0&rst=

# zsh
	sudo apt-get install zsh
	sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
	chsh?? and logout

#  词典
	sudo apt-get install stardict
	tar -zxvf  *.tar.bz2	
	sudo cp -rf /home/who/down/* /usr/share/stardict/dic
	cd /usr/share/stardict/
	sudo chmod -R 777 dic

[字典下载](http://abloz.com/huzheng/stardict-dic/zh_CN/)























