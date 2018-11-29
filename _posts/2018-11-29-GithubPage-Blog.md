---
layout: post
title: "用Github搭建属于自己的博客"
image: joon-big.jpg
video: false
---

 	用github搭建一个属于自己的博客，首先你得拥有一个github的账号，github的账号申请就不说了，下面直接开始结合jekyll搭建一个博客并绑定自己的域名：

##### 一、打开你的github页面，新建一个仓库，仓库的名字格式 ：username(你自己的用户名).github.io ，一个用户一个github博客，   如下图：

![创建仓库](http://qn.bingying.online/18-11-29/81107615.jpg)

![](http://qn.bingying.online/18-11-29/54597760.jpg)

##### 二、创建完成后，直接用HTTPS的链接或者SSH下载的项目，ssh应该都知道需要配置公钥，我的github是配置好的,直接down下来这个空的项目,进入到项目里，然后新建一个index.html文件，复制粘贴简单的代码，然后通过git上传：：

![image-20181129191333143](/Users/wangjianbing/Library/Application Support/typora-user-images/image-20181129191333143.png)

![](http://qn.bingying.online/18-11-29/29705756.jpg)

![](http://qn.bingying.online/18-11-29/220354.jpg)

![](http://qn.bingying.online/18-11-29/48512237.jpg)

![](http://qn.bingying.online/18-11-29/92481873.jpg)

##### 三、打开Setting页面，滑到中间GitHub Pages模块，选一个分支，然后在网页上地址栏上直接输入username(你的用户名).github.io，即可访问到你indexl文件中的内容

![](http://qn.bingying.online/18-11-29/68686837.jpg)

![](http://qn.bingying.online/18-11-29/78379882.jpg)

![](http://qn.bingying.online/18-11-29/35104753.jpg)

##### 四、前三部就初步建了一个博客，下面接着我们利用jekyll模板来完善你的博客，jekyll主题地址：http://jekyllthemes.org/ ，如图：

![](http://qn.bingying.online/18-11-29/3077749.jpg)

选择一个主题下载下来，（大部分主题可点击Demo预览效果），下面这是我下载下来的主题：

![](http://qn.bingying.online/18-11-29/49387835.jpg)

##### 四、本地运行jekyll项目预览效果，jekyll需要有Ruby环境的支持，请预先安装环境：

* 使用gem安装Jekyll

  ```
  $ gem install jekyll
  ```

* 安装bundler(视情况而定，看第一步操作后是否提示安装)

  ```
  $ gem install bundler
  ```

* 进入blog目录

  ```
  cd joon-master
  ```

*  开启Jekyll服务

  ```
  jekyll serve
  ```

* 命令开启服务成功后，会有一个本地的预览地址，放到网页上打开预览：(这是我更改过几个配置后显示的)，你也可以按照自己的要求来更改配置：

  ![](http://qn.bingying.online/18-11-29/7971603.jpg)

  ![](http://qn.bingying.online/18-11-29/12325716.jpg)

##### 五、配置包括内容改的差不多了，就把里面的所有文件拷贝到你的项目，然后提交到github上，这时候就可以用username(你的用户名).github.io访问到你修改的博客主页了

##### 六、绑定的域名 

* 我的是阿里云，登录阿里云（我已购买有域名，购买域名教程就不说了），找到自己的域名，点击解析：

  ![](http://qn.bingying.online/18-11-29/68042685.jpg)

* 进入解析页面，要解析三条记录，第一条类型CNAME,记录值是的仓库地址：username.github.io;第二、三条这个规定好的，github的IP,记录类型选A:

  ![](http://qn.bingying.online/18-11-29/15583220.jpg)

* 这还没完成，解析完以后，还需要一个CNAME文件做中转，在你的项目里新建一个CNAME文件，里面写上你的域名 ：格式：主机记录值.你的域名；   比如我的：blog.bingying.party，然后文件上传到git

  ![](http://qn.bingying.online/18-11-29/59367491.jpg)

* 最后查看的你的项目Setting里，下图的位置，已经主动帮你填上了你的域名，这时候用你的域名就可以直接访问你的博客啦  哈哈哈

  ![](http://qn.bingying.online/18-11-29/78843690.jpg)
