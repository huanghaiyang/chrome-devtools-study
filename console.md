# Console
+ 可以作为主控台使用，也可以嵌入到其他功能面板中使用
+ 可以显示堆栈信息或者通过线条包装并显示
+ 清空或持久化页面的输出，或者将其保存为一个文件
+ 可以根据严重等级、隐藏网络消息、正则过滤输出内容

## 打开Console
全屏展示
![](https://developers.google.com/web/tools/chrome-devtools/console/images/console-panel.png)

在其他面板下方展示
![](https://developers.google.com/web/tools/chrome-devtools/console/images/console-drawer.png)

## 作为面板打开
+ 通过快捷键 **Ctrl** + **Shift** + **J**
+ **Console**按钮

## 嵌入到其他面板中
如下步骤：
+ 快捷键**Esc**
+ 点击**Customize and control DevTools**按钮并选择**Show console**
![](https://developers.google.com/web/tools/chrome-devtools/console/images/show-console.png)

## 消息堆栈
连续且重复的消息会做为一条信息输出，前面加数字表示重复次数
![](https://developers.google.com/web/tools/chrome-devtools/console/images/message-stacking.png)

如果你希望每一条信息都单独展示，那么可以按如下方式进行设置：
![](https://developers.google.com/web/tools/chrome-devtools/console/images/show-timestamps.png)
之后的堆栈信息会以添加时间标签的方式逐行显示
![](https://developers.google.com/web/tools/chrome-devtools/console/images/timestamped-console.png)

## 历史信息
### 清空历史信息
+ 右键点击Clear console
+ 输入clear()
+ 调用console.clear()
+ 快捷键Ctrl + L

### 持久化历史信息
选中面板上方的**Perserve log**复选框，当网页刷新或变化时，日志不会被清空，除非清空控制台或者关闭当前标签页

### 保存历史信息
右键选择如图：
![](https://developers.google.com/web/tools/chrome-devtools/console/images/console-save-as.png)

### 选择执行的上下文
如图：
![](https://developers.google.com/web/tools/chrome-devtools/console/images/execution-context-selector.png)

### 过滤输出
点击按钮(![](https://developers.google.com/web/tools/chrome-devtools/console/images/filter-button.png)),显示效果如下：
![](https://developers.google.com/web/tools/chrome-devtools/console/images/filtered-console.png)

console输出的严重级别如下表所示
<table>
    <tbody>
        <tr>
            <td>All</td>
            <td>显示所有</td>
        </tr>
        <tr>
            <td>Errors</td>
            <td>console.error()</td>
        </tr>
        <tr>
            <td>Warnings</td>
            <td>console.warn()</td>
        </tr>
        <tr>
            <td>Info</td>
            <td>console.info()</td>
        </tr>
        <tr>
            <td>Logs</td>
            <td>console.log()</td>
        </tr>
        <tr>
            <td>Debug</td>
            <td>console.timeEnd() & console.debug()</td>
        </tr>
    </tbody>
</table>

### 其他选项
![](https://developers.google.com/web/tools/chrome-devtools/console/images/console-settings.png)



