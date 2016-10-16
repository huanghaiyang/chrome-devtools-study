# Security
检测当前页面是否是安全的</br>
如果当前页面是安全的，则会显示**This page is secure (valid HTTPS).**
![](https://developers.google.com/web/tools/chrome-devtools/images/overview-secure.png)

点击**View certificate**按钮，可以查看证书信息
![](https://developers.google.com/web/tools/chrome-devtools/images/view-certificate.png)
如果当前页面是不安全的，则会显示**This page is not secure.**

Secutiry可以检测两种类型的不安全页面
+ 如果当前页面是通过HTTP请求的，则请求来源（origin）会被标示为不安全的
![](https://developers.google.com/web/tools/chrome-devtools/images/overview-non-secure.png)
+ 如果网页是通过HTTPS请求，但内容是通过HTTP传输，那么网页仍然被标示为不安全的
![](https://developers.google.com/web/tools/chrome-devtools/images/overview-mixed.png)
