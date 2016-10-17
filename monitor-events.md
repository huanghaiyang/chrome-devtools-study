# Console
## Monitor Events (事件监听)
+ 使用monitorEvents()方法对页面元素进行事件监听，记录事件触发
+ 使用unmonitorEvents()解除事件监听
如果需要对document.body的click事件做监听，可以添加如下代码到console
```
monitorEvents(document.body, "click");
```
此时任何body上的任何点击事件都会被记录下来，显示在console上                         
解除事件监听可以输入：
```
unmonitorEvents(document.body);
```
此代码解除了body上的所有事件监听，如果想单独解除click事件监听，可以执行
```
unmonitorEvents(document.body, 'click');
```

## View event listeners registered on objects(查看对象上的事件监听器)
getEventListeners()方法返回了对象上注册的事件监听器                
输入
```getEventListeners(document);
```
返回document上的的事件监听列表
![](https://developers.google.com/web/tools/chrome-devtools/console/images/events-call-geteventlisteners.png)
如果同一个事件上被绑定了多个事件处理函数，则会有如下显示
![](https://developers.google.com/web/tools/chrome-devtools/console/images/events-geteventlisteners_multiple.png)