## 软件的高级玩法

后面还会不定期更新的

本仓库收集本人的多年使用经验，并不定时更新，主要面向一些能力无法满足需求的用户

阅读本文前，建议查看词汇含义，并拥有一定的搜索技巧

[点我](#目录)进入目录

本文中词汇大致含义：

Root：超级用户，拥有手机最高权限，能修改系统，通常普通人无法使用到，一般通过刷机刷入 Magisk 获得，这里不阐述

框架：例如 VirtualXposed，能弥补上述情况，软件需要安装在这里面，自行搜索相关教程（如果兼容性不好，请尝试虚拟机）

模块：Xposed 模块，大致可理解为能修改应用运行逻辑的程序

HTTPS：安全的 HTTP，对于大众来说直接理解为网页的协议即可，有兴趣可以深入研究

ADB：安卓调试桥，有更高权限（用户 < Shell(ADB) < 系统 < Root），一般你需要数据线连接一台电脑以使用它，后续会出教程

### 目录

* [安卓软件](#安卓软件)
  * [微信](#微信)
    * [旧版本登录](#旧版本登录)
    * [视频号下载](#视频号下载)
    * [清空性别](#清空性别)

### 安卓软件

#### 微信

##### 旧版本登录

目前有两种方案：降级和改包

降级：先用 7.0.12 以上版本登录，再使用 adb install -d -r /旧版微信/安装包的路径.apk 执行降级，优先选择此方案

改包：参考 https://blog.csdn.net/Jiangling6998/article/details/125039663

但请**一定要注意防封**，也不要用主账号尝试

##### 视频号下载

需要 Root/框架 环境

打开抓包软件（如 ProxyPin，记得启用 HTTPS 代理），运行抓包

打开微信，进入要下载的视频，直到列表出现 http://findercsy.video.qq.com/xxx/xxxx/stodownload 开头的链接

替换链接中的 findercsy 为 finder，然后通过浏览器等方式下载即可

无 Root 时，请安装 JustTrustMe 模块，作用域勾选微信，否则会无法抓包

##### 清空性别

需要 Root/框架 环境

下载 GameGuardian 并安装，初始化

打开微信，设置性别页面

打开 GG，搜索（男为1，女为2），然后反复切换，重复搜索，直到剩下两三个值

然后批量修改，值为 0，并冻结

保存，返回主页（微信崩溃是正常情况）

然后就成功了

##### 待更新
