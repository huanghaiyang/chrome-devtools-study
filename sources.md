# Sources

## 设置断点
+ 最常见的基本用法就是将断点加到指定代码行上，而且可以配置为条件触发
+ 断点可以被一个通用条件触发，例如一个事件、一个节点变化、或者一个未捕获的异常

## 将断点设置在代码行上
打开Sources面板，选择左侧的File Navigator子面板</br>
提示：如果当前的代码被压缩，你可以点击(![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/pretty-print.png))将代码格式化
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/line-number-breakpoint.png)

如果当前的表达式跨行，而你想讲断点放到中间行上，那么DevTools会跳过表达式，将断点防止到下一个表达式的开始行上，例如你想将断点放置在第4行，实际上，DevTools会将其放在第6行
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/mid-expression-breakpoint.png)

## 给断点添加条件
指定条件为true时，断点触发

操作如下：

在代码行号上右键选择**Add conditional breakpoint**创建一个条件断点，如果已经有一个断点，则选择**Edit breakpoint**，在文本框中填入条件并回车
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/adding-condition.png)
注意条件断点颜色为为金黄色
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/conditional-breakpoint.png)

## 删除或禁用断点
禁用：在代码行上右键选择**Disable breakpoint**
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/disable-breakpoint.png)

移除：在代码行上右键选择**Remove breakpoint**

也可以在**Breakpoints **面板上进行操作,如下图
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/breakpoints-pane.png)

禁用所有断点可以点击(![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/deactivate-breakpoints-button.png))按钮

## 给DOM节点变化设置断点
当节点添加、删除、变化时，如果你不知道是哪部分代码起了作用，那么你可以给节点添加断点帮助你定位有效代码
切换到**Elements**面板，为DOM设置断点
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/dom-change-breakpoint.png)

提示：这里的断点选项是可以多选的

条件解释如下：
+ **Subtree modifications** 当前节点的子节点被删除，添加或者子节点的内容发生改变时触发，注意子节点属性变化或者当前节点本身发生变化并不会触发断点
+ **Attributes modifications**  当前节点的属性被添加、删除或者属性值发生改变时触发
+ **Node Removal** 当前节点被移除时触发
效果如下：
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/dom-breakpoint-indicator.png)

你可以在**Ellements**的子面板**DOM Breakpoints**管理和查看所有的DOM断点，用法简单
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/dom-breakpoints-pane.png)
或者在**Sources**的**DOM Breakpoints**查看，功能同上
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/dom-breakpoints-pane-sources.png)

## 为XHR添加断点
有两种方法可以为XHR添加断点：

1. 当XHR处于生命周期的特定状态时，如```readystatechange```、```load``` ...
2. 匹配XHR的请求地址

匹配XHR请求地址的方式为：打开**Sources**的**XHR Breakpoints**的子面板
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/xhr-breakpoints-pane.png)
点击添加按钮，输入文本字符并回车

## 给事件添加断点
打开**Sources**的**Event Listener Breakpoints**子标签面板
一级显示的是事件分类
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/event-listener-breakpoints-pane.png)
二级显示的是具体事件类型
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/expanded-event-listener-breakpoints-pane.png)

## 给未捕获的异常添加断点
如果你的代码抛出了异常而且你不知道哪里出现了错误，那么可以在**Sources**面板上点击**pause on exception**按钮(![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/pause-on-exception-button.png))

## 调试代码
利用此功能我们可以监听数据对象的改变并且可以更加直观的了解到页面到底发生了什么，你可以利用脚本修改数据值，甚至修改脚本本身</br>
通常我们会在设置完断点后，返回到当前页面进行操作直到断点被触发，断点触发操作阻塞了当前页面的JavaScript脚本，并且将DevTools切换到**Sources**面板，高亮显示当前设置断点的代码行，此时你可以钻取代码并查看数据值。
+ 在代码执行前或执行过程中进行监听或者实时修改代码并使其生效
+ 替代console
+ 启用Async call stack(堆栈异步调用)让异步函数调用栈过程更清晰
+ 在调用栈中用黑盒来隔离并隐藏第三方代码
+ 用命名函数替代匿名函数更易于提高调用栈的可读性

## 逐步操作
工具栏包含了这些按钮![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/image_7.png),分别表示如下：
<table>
    <tbody>
        <tr>
            <td>按钮</td>
            <td>操作</td>
            <td>描述</td>
        </tr>
        <tr>
            <td>![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/image_8.png)</td>
            <td>继续执行</td>
            <td>继续执行执行下一个断点</td>
        </tr>
        <tr>
            <td>![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/image_9.png)</td>
            <td>持续执行</td>
            <td>断点不阻塞，持续执行500ms</td>
        </tr>
        <tr>
            <td>![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/image_10.png)</td>
            <td>跳过</td>
            <td>执行下一行</td>
        </tr>
        <tr>
            <td>![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/image_11.png)</td>
            <td>跳入</td>
            <td>跳入到函数内部</td>
        </tr>
        <tr>
            <td>![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/image_12.png)按钮</td>
            <td>跳出</td>
            <td>跳出当前函数</td>
        </tr>
        <tr>
            <td>![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/image_13.png)</td>
            <td>禁用断点</td>
            <td>禁用所有断点</td>
        </tr>
        <tr>
            <td>![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/image_14.png)</td>
            <td>异常暂停</td>
            <td>异常发生时自动暂停代码执行</td>
        </tr>
    </tbody>
</table>

## View properties by scope
主要用于查看作用域中定义的属性,
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/scope-pane.png)
其中，有些属性会是颜色较浅的，表示不可枚举类型，颜色较亮的为属性，可枚举
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/enumerables.png)
constructor为构造函数，不可枚举，confirm为属性，可枚举

## The call stack
如图所示，清楚的展示了函数的调用顺序，注意，调用顺序为从下往上
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/image_15.png)
分别为：
+ index.html中第50行触发了onclick事件
+ 调用setone()方法
+ 调用setall()方法

## Enable the async call stack
激活**Async**复选框，能够查看当前函数的异步调用方式

## Blackbox third-party code
使用此功能能够将第三方的代码调用从你的call stack 中隐藏起来
before blackbox:
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/before-blackbox.png)
after blackbox:
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/after-blackbox.png)
对比可以看到，jquery的调用已经在call stack中被隐藏起来

想要开启此功能，需要如下步骤：
+ 打开DevTools settings
    ![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/open-settings.png)
+ 选择Blackboxing
    ![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/blackbox-panel.png)
+ 点击 **Add pattern**
    ![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/add-pattern.png)
+ 选择下拉中的blackbox选项
+ add

## 在任一页面运行代码片段
### 创建代码片段

![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/create-snippet.png)

### 运行代码片段
点击按钮![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/run.png)运行或者
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/evaluate-in-console.png)

### 查看代码片段的本地修改历史
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/local-modifications.png)
结果   
![](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/snippet-history.png)

