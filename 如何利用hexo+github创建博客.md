#小白利用hexo和github搭建博客
##前言：
纯新手小白，转行自学java途中，想写点东西，记录自己的成长过程。因此，花了一天的时间，游览各个大佬的文章，学着用hexo和github搭建自己的博客。
##一、所需要的环境

1. **安装Node.js()**   
[http://nodejs.cn/download/](http://nodejs.cn/download/ "官方下载nodejs")  
配置环境变量，windows下安装配置环境，一键完成很简单。

1. **安装git（必须）**     
可以查看廖雪峰老师的git教程[https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)学习安装  
下载地址：[https://git-for-windows.github.io/](https://git-for-windows.github.io/ "官方下载git")  
注册github账号:[https://github.com/](https://github.com/ "官网注册")  
配置SSH-key:  
[https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001374385852170d9c7adf13c30429b9660d0eb689dd43a000](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001374385852170d9c7adf13c30429b9660d0eb689dd43a000 "如何配置ssh")。  
创建名为userName.github.io的仓库,userName是你申请的用户名。
##二.安装hexo
1. 安装Hexo:  
	> 右键git bash,输入`npm install -g hexo`  

2. 初始化Hexo:

	> 自定义创建一个文件夹（用来放置你的博客）,点击该文件夹,输入  > `hexo init`  

3.然后生成部署文件，启动本地服务  
	> hexo g  或者hexo generate
	 hexo s  或者hexo server，可以在http://localhost:4000/ 查看
  
至此hexo已经安装完毕了,我安装过程中出现了以下**问题**：  

 在hexo install过程中可能出现  
`npm WARN deprecated swig@1.4.2: This package is no longer maintained`  
只是说这个包不再维护了，后面好像并不影响使用，当然你也可以`npm -g install npm`，更新安装。
##三、布置博客
1. 熟悉git的简单操作
	> 选中你的文件夹 `git init` ，创建仓库  
	> `git add.``git commit -m"标记"`，提交文件修改
	> `git remote add origin https://github.com/Scyzin/scyzin.github.io.git`  与你的github仓库连接  
	> `git push -u origin master`，将你的修改上传到github上。  
1. 博客主题更换
	> hexo默认的主题是landscape，在themes文件夹下，可以使用别人开发好的主题，这里有很多，我使用的是这一个: https://github.com/litten/hexo-theme-yilia   
	> 下载之后将文件夹整个复制到`D:\blog\themes`目录下，再修改`D:\blog`
 的下_config.yml文件里的theme：`theme: hexo-theme-yilia`。
1. 部署配置
	> 配置到github对应的仓库中:  
	> 
	> 1.为hexo安装git插件:`npm install --save hexo-deployer-git`，否则会出现 `hexo d`时会出现 ERROR Deployer not found: git  
	> 2.修改`D:\blog`
 的下_config.yml文件  
	> 
	> deploy:   
	> type: git   
	> repo: https://github.com/Scyzin/scyzin.github.io.git   
	> branch: master  
	  


> 加入如下配置：  
>  

冒号后面都必须有空格。  
1. Hexo配置文件说明:D:\blog`的下_config.yml  
常用的配置熟悉下就会了，这里可以选择学习一个扩展配置。[http://blog.csdn.net/u013082989/article/details/70144934?locationNum=3&fps=1](http://blog.csdn.net/u013082989/article/details/70144934?locationNum=3&fps=1 "一个hexo扩展配置")
1. `hexo d`，将博客发布在github.io上。  

**至此你就可以直接通过scyzin.github.io访问你的博客。当然你也可以选择购买域名，绑定自己的地址访问。**  
##四、hexo常用命令  

    hexo new "postName" #新建文章
其中my new post为文章标题，执行命令后，会在项目\source_posts中生成my new post.md，用markdown编辑器打开编辑就行了。  

当然，也可以直接在\source_posts中新建一个md文件，我就是这么做的。**

    hexo new page "pageName" #新建页面
    hexo generate #生成静态页面至public目录
    hexo server #开启预览访问端口（默认端口4000，'ctrl + c'关闭server）
    hexo deploy #将.deploy目录部署到GitHub
    hexo help # 查看帮助
    
简写:

    hexo n == hexo new
    hexo g == hexo generate
    hexo s == hexo server
    hexo d == hexo deployexo version #查看Hexo的版本
    
##  未完待续
scyz  
一个在自学java的渣硕  
2017/11/12 14:26:17 

    





