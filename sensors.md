# 传感器：地理位置&平衡仪
用来模拟通用移动设备上的传感器

## 访问传感器控制器
1.打开DevTools菜单
2.选择 More Tools, 点击Sensors

![](https://developers.google.com/web/tools/chrome-devtools/device-mode/imgs/navigate-to-sensors.png)

<font color=blue>提示：如果你的脚本中包含了探测传感器的代码，那么在调用传感器模拟后，需要重新加载当前页面才可以使代码生效</font>

## 覆盖地理位置数据
不同于桌面，移动设备通常使用GPS来定位地理位置，在Sensors面板，你可以通过输入坐标来模拟地理位置

勾选**Emulate geolocation coordinates**复选框，填入坐标

![](https://developers.google.com/web/tools/chrome-devtools/device-mode/imgs/emulation-drawer-geolocation.png)

当地理位置数据不可用时，可以使用模拟器覆盖```navigator.geolocation```属性

## 模拟平衡仪
![](https://developers.google.com/web/tools/chrome-devtools/device-mode/imgs/emulation-drawer-accelerometer.png)