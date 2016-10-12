# network
主要显示了网络资源加载耗时，测量站点的网络性能，具体显示内容包括：HTTP请求及相应头，cookies等</br>
如下图所示
![](https://developers.google.com/web/tools/chrome-devtools/network-performance/imgs/network-panel.png)

+ 记录和分析网络活动
+ 查看收集到的加载信息和特殊资源
+ 对资源进行过滤和排序显示
+ 保存、复制、清空网络记录
+ 按需自定义网络面板

网络面板分为五个显示区域，各自表示如下：
1.Controls 控制面板的显示和功能
2.Filters  过滤请求列表的显示内容
3.Overview 资源的并发请求
4.Requests Table 详细的显示了资源请求的时间线
5.Summary 显示了资源的请求数量，数据传输大小和加载时间

![]{https://developers.google.com/web/tools/chrome-devtools/network-performance/imgs/panes.png}

## Request Table各显示列的含义
+ Name 资源名称
+ Status HTTP状态
+ Type MIME类型
+ Initiator 请求发起者
  * Parser HTML解析
  * Redirect 资源重定向
  * Script 脚本请求
+ Size 从服务器已经接收的资源大小
+ Time 请求时间
+ Timeline 已瀑布流的形式显示各资源的加载时序

## 记录网络活动
按钮![](https://developers.google.com/web/tools/chrome-devtools/network-performance/imgs/record-on.png)表示记录网络活动，相反为![](https://developers.google.com/web/tools/chrome-devtools/network-performance/imgs/record-off.png)

## 快照
点击![](https://developers.google.com/web/tools/chrome-devtools/network-performance/imgs/filmstrip-enabled.png)按钮，在资源加载过程中显示网页的各时间点的快照,如图
![](imgs/record_screenshot.png)

## 查看DOMContentLoaded和load事件信息
如图蓝色的表示DOMContentLoaded加载时间
![](https://developers.google.com/web/tools/chrome-devtools/network-performance/imgs/domcontentloaded.png)
橙色的表示load加载时间
![](https://developers.google.com/web/tools/chrome-devtools/network-performance/imgs/load.png)

## 查看资源详细信息
点击一个资源，会显示它的详细信息,四个标签页内容分别表示如下：
+ Headers http请求头
+ Preview JSON、图片和文本预览
+ Response http返回内容
+ Timing 资源在请求阶段的详细时间分布
  * Queuing 队列时间
  * Stalled 挂起时间
  * Request/Response 请求和响应
  * Request sent 发送耗时
  * Waiting (Time to first byte (TTFB)) 等待时间（直到服务第一次返回）
  * Content Download 下载时间
