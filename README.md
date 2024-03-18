# 我的个人图床

> [GitHub](https://github.com/wefashe/git-images)+[Typora](https://www.typora.net/#windows)+[PicGo](https://github.com/Molunerfinn/PicGo/releases)+[jsDelivr](https://www.jsdelivr.com/?docs=gh "jsDelivr 是一个免费开源的 CDN 解决方案,是首个「打通中国大陆与海外的免费CDN服务」")



**搭建Github图床**

![](https://raw.gitmirror.com/wefashe/git-images/master/images/202403181027645.png)



**生成Access ToKen**

Github头像 -> Settings -> Developer settings -> Personal access tokens -> Tokens (classic)：

![](https://raw.gitmirror.com/wefashe/git-images/master/images/202403181033161.png)

![](https://raw.gitmirror.com/wefashe/git-images/master/images/202403181034949.png)

`Expiration`代表这个token的过期时间，No expiration 永不过期，自己根据实际情况设置。访问权限范围选择`repo`即可。创建成功后会获得一串代码，记得把代码保存，这个代码只会当前显示，之后就看不到了。



**Typora+PicGo搭配使用**

<img src="https://cdn.jsdelivr.net/gh/wefashe/git-images@master/images/20200310202556.png">

<img src="https://cdn.jsdelivr.net/gh/wefashe/git-images@master/images/20210112153557.png">



**jsDelivr CDN使用**

CDN的两个功能：

基础功能：可以提供静态文件内容
主要功能：加速内容获取，提高访问速度  

设定自定义域名：`https://cdn.jsdelivr.net/gh/用户名/仓库名@分支名` 或 `https://fastly.jsdelivr.net/gh/用户名/仓库名@分支名`

例如：

`https://cdn.jsdelivr.net/gh/wefashe/git-images@master`

<img src="https://cdn.jsdelivr.net/gh/wefashe/git-images@master/images/20210112155305.png">

**返回URL**

`https://cdn.jsdelivr.net/gh/用户名/仓库名@分支名/指定的存储路径/文件名`

例如

`https://cdn.jsdelivr.net/gh/wefashe/git-images@master/images/20210112153045.png`

<img src="https://cdn.jsdelivr.net/gh/wefashe/git-images@master/images/20210112175811.png">



**Github RAW 加速服务**

jsDelivr：<https://cdn.jsdelivr.net/gh/wefashe/git-images@master/images/20240318093020.png>

githubusercontent：<https://raw.githubusercontent.com/wefashe/git-images/master/images/20240318093020.png>

当上述两种都不能使用时，可以使用 [Github RAW 加速服务](https://gitmirror.com/raw.html)，只需要将上面githubusercontents图片链接中的`raw.githubusercontent.com`简单替换成`raw.gitmirror.com`即可，

gitmirror：<https://raw.gitmirror.com/wefashe/git-images/master/images/20240318093020.png>

可以设定自定义域名：`https://raw.gitmirror.com/用户名/仓库名/分支名`

例如：

`https://raw.gitmirror.com/wefashe/git-images/master`

![](https://raw.gitmirror.com/wefashe/git-images/master/images/202403181017592.png)

**返回URL**

`https://raw.gitmirror.com/用户名/仓库名/分支名/指定的存储路径/文件名` 





**图片压缩**

在没有经过任何处理的情况下，图片都是原图上传的，实际浏览过程中会发现图片加载很慢，尤其是在国内访问Github的情况下。

我们有时候并不需要很高清的图片，并且更希望图片能快速加载出来。因此可以在图片上传之前进行压缩处理。

PicGo集成了很多插件，可以直接在`插件设置`里搜索`compression`，[compression](https://github.com/Redns/picgo-plugin-compression) 它可以在图片上传前自动对图片完成压缩。压缩后的图像质量也还可以，关键是文件很小，一般都只有几十k，能满足快速加载的需求。

![](https://cdn.jsdelivr.net/gh/wefashe/git-images@master/images/20240318093941.png)
