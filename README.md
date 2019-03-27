# BT
bt

yum install -y wget && wget -O install.sh http://download.bt.cn/install/install.sh && sh install.sh


一些微信第三方的链接：
https://blog.csdn.net/xzli2008/article/details/46700495
https://blog.csdn.net/xzli2008/article/details/46700495


四个步骤：
https://blog.csdn.net/SHENLINGSUIFENG/article/details/51006206

全网发布接入测试：
https://blog.csdn.net/joelingwei/article/details/72980886

component_access_token篇：
https://blog.csdn.net/joelingwei/article/details/72876760
https://www.cnblogs.com/dige1993/p/7078351.html

微信官方文档
https://open.weixin.qq.com/cgi-bin/showdocument?action=dir_list&t=resource/res_list&verify=1&id=open1453779503&token=&lang=zh_CN


精美网页
https://blog.csdn.net/wangchaoqi1985/article/details/80382187


网页微信授权
https://www.cnblogs.com/0201zcr/p/5133062.html


公众平台返回码
https://mp.weixin.qq.com/wiki?t=resource/res_main&id=mp1433747234

开放平台返回码
https://open.weixin.qq.com/cgi-bin/showdocument?action=dir_list&t=resource/res_list&verify=1&id=open1419318634&token=&lang=zh_CN

http://www.zjychina.cn/p/1238731.html



我说一下我的SLB方案，我是用多台云主机，来实现大带宽，单独买带宽太贵了。 
 
1台高级方案，专门用来跑程序，用的商业版litespeed保证性能。就是说，所有的后端程序，都是由这台高级方案解决。 
N台前端，来反向代理后端，使用内网IP，这样没有带宽限制。 
使用SLB整个N台前端，达到整合N台前端的总带宽，供给SLB使用的目的。 
 
这样，访客访问的时候，首先通过的是SLB，再走过某台前端的nginx，再反向代理到后端的程序。 
其中某台前端，使用nginx搭配一定程度的缓存，也能增加网站的访问速度。 




