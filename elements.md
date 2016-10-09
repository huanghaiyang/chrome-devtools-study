# 页面和样式的检查及修改
检查和实时修改HTML内容和样式
![](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/imgs/elements-panel.png)

+ 检查修改DOM树上的任意节点(Elements 面板)
+ 对选中节点上查看并修改CSS样式规则，使其生效(Styles 面板)
+ 查看和编辑元素的盒模型(Computed 面板)
+ 本地查看所做的修改(Sources 面板)

## 实时修改元素节点
![](edit node.png)

## 实时修改样式
除了灰色部分的UA样式定义，其他均可以进行修改,而且修改部分在网页重新加载后就会丢失
![](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/imgs/edit-property-name.png)

## 检查和编辑盒模型参数
盒模型中的参数均可以修改，只要点击输入值即可
![](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/imgs/computed-pane.png)
盒模型的四边**top**、**bottom**、**left**、**right**分别包含并显示了当前节点的**padding**、**border**和**margin**值

一个绝对定位的元素同样含有**top**、**bottom**、**left**、**right**属性值
![](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/imgs/computed-non-static.png)

## 查看修改的样式内容
![](css local change.png)
查看当前页面的修改历史步骤如下：
1.在Style面板，点击被你修改的文件，DevTool会转到Sources面板
2.右键文件
3.选择Local modifications

