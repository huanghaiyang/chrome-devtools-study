# Chrome DevTools概述

## 访问DevTools

在已打开的浏览器页面：
+ 选择菜单![菜单按钮](https://developer.chrome.com/devtools/devtools/images/chrome-menu.png) > Tools > Developer tools
+ 右键点击页面元素，选择**检查(N)**

通过快捷键方式：
+ ```Ctrl``` + ```Shift``` + ```I```  打开
+ ```Ctrl``` + ```Shift``` + ```J```  打开并定位到控制台(Console)
+ ```Ctrl``` + ```Shift``` + ```C```  打开并切换到检查元素模式

## DevTools窗口
如下所示：
![DevTools窗口](https://developer.chrome.com/devtools/devtools/images/devtools-window.png)
包含功能：
+ [Elements](elements.md)
+ [Resources](resources.md)
+ [Network](network.md)
+ [Sources](sources.md)
+ [Timeline](timeline.md)
+ [Profiles](profiles.md)
+ [Audits](audits.md)
+ [Console](console.md)

同时可以使用```Ctrl``` + ```[``` 或者 ```Ctrl``` + ```]``` 切换功能面板

## 检查DOM节点及样式
使用[Elements](elements.md)面板可以查看DOM树结构，允许检查和编辑DOM元素。
![Elements面板](https://developer.chrome.com/devtools/devtools/images/elements-panel.png)
[详细介绍](https://developer.chrome.com/devtools/devtools/docs/dom-and-styles)

## 控制台
Javascript console 提供了两个主要的功能来测试页面和应用
+ 在开发过程中记录诊断信息
    ```console.log()``` 和 ```console.profile()```
+ 一个shell风格的可与文档和DevTools交互的控制台
    可以使用```$()```命令选择文档元素或者使用```profile()```函数开启cpu分析功能

如下所示：
![Console面板](https://developer.chrome.com/devtools/devtools/docs/console-files/expression-evaluation.png)
[详细介绍](https://developer.chrome.com/devtools/devtools/docs/console)

## 调试JavaScript
如下所示:
![sources面板](https://developer.chrome.com/devtools/devtools/images/js-debugging.png)
[详细介绍](https://developer.chrome.com/devtools/devtools/docs/javascript-debugging)

## 改善网络性能(性能监控)
通过**Network**功能可以实时查看资源的请求和下载耗时等详细信息
如下所示:
![network面板](https://developer.chrome.com/devtools/devtools/images/network-panel.png)
[详细介绍](https://developer.chrome.com/devtools/devtools/docs/network)

## 审查和建议
Audit功能面板能够通过网页的加载进行分析，之后提供建议与优化方法来降低页面的加载耗时并提高页面的响应速度
如下所示:
![audit面板](https://developer.chrome.com/devtools/devtools/images/audits-panel.png)

## 提高渲染性能
Timeline面板提供了一个完整分析页面或者app的具体时间花费的详细信息，从加载资源到解析javascript，计算样式以及页面绘制
如下所示
![timeline面板](https://developer.chrome.com/devtools/devtools/images/timeline-panel.png)
[详细介绍](https://developer.chrome.com/devtools/devtools/docs/timeline)