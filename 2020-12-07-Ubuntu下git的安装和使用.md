> 本人初学GitHub，对git了解的不够深入，文章中有不足或者错误欢迎大家来改正。

##  1.git的安装
首先查看git命令是否安装，如果没有安装，则通过命令apt来进行安装。

```javascript
git --version				#查看当前git的版本
apt-get upgrade -y			#先更新apt，防止git安装不完全
sudo apt-get install git	#如果系统没有git，则通过此命令进行安装
```

**安装完成后对git进行配置**

```javascript
git config --global user.name "xxx"		#把用户名写入git
git config --global user.email "xxx"	#把邮箱写入git
```

**对GitHub密钥进行配置**
```javascript
ssh-keygen -t rsa		#生成密钥
cd ~/.ssh				#进入密钥文件目录
cat ~/.ssh/id_rsa.pub	#查看密钥
```

对id_rsa.pub文件内容进行复制，然后进入GitHub网站的[settings](https://github.com/settings/profile)，配置ssh，新建一个ssh，把刚才复制的内容粘贴进去，标题随便命名。

![把复制的内容添加到这里](https://img-blog.csdnimg.cn/20201207183325180.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZqYWxqZGE=,size_16,color_FFFFFF,t_70#pic_center)

```javascript
ssh -T git@git.oschina.net	#测试连接是否通畅
```

然后就可以上传文件了

##  2.git的使用

```javascript
git init						#新建一个空仓库
cd .git							#进入目录
git add <文件名>		
git commit -m "项目名"			#把文件提交
git remote add origin <仓库地址>	#把文件提交到指定仓库
git push origin master			#添加到分支
```


