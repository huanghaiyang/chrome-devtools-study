# Application
检查和管理Storage、Databases、Caches ...

## TL;DR
+ 查看和编辑local、session storage
+ 检查和修改IndexedDB数据库
+ 执行Web SQL查询
+ 查看Application和Service Worker缓存
+ 清空所有

## Local Storage
使用Local Storage存储键值对数据（KVP）,以及查看、修改、删除操作
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/local-storage.png)
使用方法：
+ 在某一个key 或者 value上双击编辑
+ 双击一个空行添加一个KVP
+ 点击![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/delete.png)删除选定的某一个行KVP
+ 点击![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/refresh.png)刷新

## Session storage
操作同Local Storage

## IndexedDB
查看、修改和删除IndexedDB数据
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/idb-tab.png)
可以包含多个激活的IndexedDB数据库

点击其中一个数据库，查看数据库的security origin/ name/ version属性

![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/idb-db.png)
展开数据库查看KVP数据
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/idb-kvps.png)

点击其中的一个KVP行，可以对值进行编辑、删除操作
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/idb-edit.png)
之后点击刷新按钮，查看编辑结果

编辑**Start From Key**文本框内容，对数据进行过滤显示
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/idb-filter.png)

## Web SQL
查询和修改Web SQL数据库

![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/web-sql-console.png)
点击数据库名称会打开一个database console控制台，输入查询语句查询数据
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/web-sql-console.png)
点击数据表名称，可以查看全部数据
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/web-sql-table.png)
你可以
+ 在数据列表中更新数据（但不可以通过database console操作）
+ 点击table header排序
+ 修改不会即时生效，需要点击刷新按钮
+ 输入一个space-separated 或 comma-separated的多个列名称，可以控制列的显示

## Application Cache
查看资源的缓存情况
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/appcache.png)
每一行都展示了一个资源，其中Type列的取值含义如下：
+ Master mainfest master
+ Explicit 在mainfest中定义的资源
+ Network 表示资源必须通过网络获取
+ Fallback 上一个url, 记录后退操作的url地址

列表底部的按钮显示了当前网络的连接和Application缓存状态，其中缓存状态可有以下几种取值：
+ IDLE缓存无需更新
+ CHECKING 正在检查更新
+ DOWNLOADING 资源正加入缓存中
+ UPDATEREADY 新版本更新可用
+ OBSOLETE 缓存被删除

## 清空
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/clear-storage.png)

## Cookies
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/cookies.png)
可行操作
+ 查看cookie的详细信息，如name/value/domain/size...
+ 删除一个cookie/或者删除一个domain下的所有cookie，或者删除所有domain下的所有有cookie

注意：你只能查看和删除cookie，而不能进行修改操作

cookie列表中的每一列含义如下：
+ Name 名称
+ Value 值
+ Domain 域名
+ Path 路径
+ Expires / Maximum Age 过期时间或最大生命时间,注意： session cookie的值始终为'session'
+ Size bytes size
+ HTTP 如果次出勾选，表示cookie只能通过HTTP使用，而不能通过js代码进行修改
+ Secure 如果此处勾选，表示此条cookie必须通过加密传输

## Organize resources by frame
按页面嵌套结构展示所有资源信息
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/frames.png)

按如下操作，进入到Resources面板查看资源信息
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/resource.png)

Resources中的资源可以按照**Group by folder**组织资源的显示结构
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/group-by-folder.png)
如果去掉**Group by folder**状态，资源只能够按照frame结构进行展示
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/no-folders.png)

## Organize resources by domain and folder
资源默认按照domain和文件夹结构进行展示
![](https://developers.google.com/web/tools/chrome-devtools/manage-data/imgs/sources.png)
