# Git和Github是托管代码和资料的工具。

1.github使用  
 1.1）先注册github.com的账号，官方网站: https://github.com/  
 1.2）创建账号后，得先创建仓库才能放我们想放的代码或者资料文件，
  点New repository按钮，在设置权限的的时候一般选public，因为它是免费的，private是收费的也可以使用。
  
2.windows 安装git  
 2.1）下载网址: http://code.google.com/p/msysgit/downloads/list  
 2.2）下载完后，安装，一般情况下选默认的安装路径就可以。
 
 3.配置Git  
  3.1）生成本机密钥  
     $ ssh-keygen -t rsa -C "abcd@efgh.com" //邮箱同上，或者其它名称  
     得到2个文件，一个是id_rsa,一个是id_rsa.pub，打开id_rsa.pub文件复制里面的内容。  
     
4.回到github上配置一下ssh key  
  4.1）点击我的头像里有一个setting按钮，在左侧出现一列选项，点击左侧的SSH Keys，点击右侧的Add SSH Key，出现添加SSH Key的界面
    把title和key填上就可以了。
    
5.验证一下是否设置成功  
   在git bash下输入如下命令：  
$ ssh –T git@github.com

5.2)配置一下用户名和邮箱：  
git config –global user.name “用户名”  

git config –global user.email “邮箱”  

即完成了Git和Github的配置。  

6.先克隆一份代码  
$ git clone git@github.com:xxxxx/xxxx.git  
本地库关联远程库，在本地仓库目录运行命令：  
$ git remote add origin git@github.com:xxxxx/xxxx.git  

同步项目  
$ git pull git@github.com:xxxxx/xxxx.git

本地的上传到仓库上去了  
$ git add .  
提示信息  
$ git commit –m “Nxxxv1.0版本”  
提交代码  
$ git push git@github.com:xxxxx/xxxx.git


7.Git的一些常用命令   
<http://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html>


 8. 合并远端分支到本地分支的两种方式   
 git merge origin/master


