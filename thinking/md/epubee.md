### 电子书下载

*网址：http://cn.epubee.com （原网站VIP可以随时无限次下载，非VIP只能凌晨1点-7点下载三次）*

**破解步骤**
1. 下载chrome浏览器
2. 安装chrome插件ReRes (作用：js拦截，建立远程js和本地js的关系。当网站访问远程js时，会自动访问本地修改过的js)
3. 该网站发起请求的js代码路径：http://cn.epubee.com/app_books/manager.js，将其下载到本地
4. 在本地js代码中将下图位置的isVip替换成1
    ![下载到本地的js代码](https://github.com/caoweiwei/qz.read.thinking.in.java/blob/master/thinking/md/png/WX20190219-225910%402x.png "本地代码")
   
5. 在第二步安装的ReRes插件中，将远程路径http://cn.epubee.com/app_books/manager.js 和下载到本地的路径(如:file:////Users/caoweiwei/Downloads/faker.js)建立绑定关系
6. 以后访问http://cn.epubee.com网站就可以和VIP一样随时不限次数的下载电子书了
    

