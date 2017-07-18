## 背景
王者农药荣耀战区，想选个人少点的区拿排名，人又不可能真实过去，咋办？

## 准备工作
你得有台mac，装了xcode的，版本至少要能支持你的ios设备。

## 实施工作
### 创建项目
![](https://ws3.sinaimg.cn/large/006tKfTcgy1fhntbj0xl4j312u0q5ada.jpg)
随便新建一个ios项目就成，一路next把工程新建好。

### 设置schema
![](https://ws1.sinaimg.cn/large/006tKfTcgy1fhntclav24j30uw0e7ach.jpg)
在options中开启模拟gps，并选择你期望的地域地址。
![](https://ws2.sinaimg.cn/large/006tKfTcgy1fhntcuyojpj30p80ecmzg.jpg)
xcode默认只提供了几个地域供你选择，如果你期望自己设定一个地址，可以选择`add GPX file to project`。

GPX file是一个xml文件，格式如下：

```
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<gpx xmlns="http://www.topografix.com/GPX/1/1" creator="MyGeoPosition.com" version="1.1" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd">
    <wpt lat="25.7714505528" lon="123.5385131836">
        <name>钓鱼岛</name>
        <src>MyGeoPosition.com</src>
        <link>http://mygeoposition.com</link>
    </wpt>
</gpx>

```

至于如何获取到你所需要的gps信息，可以访问[http://www.gpsspg.com/maps.htm](http://www.gpsspg.com/maps.htm)获得。

### 添加真实设备
- 用usb线连接你的iphone

![](https://ws4.sinaimg.cn/large/006tKfTcgy1fhntdb1jjcj30c206swfd.jpg)

- 点击工程右侧的设备选择

![](https://ws3.sinaimg.cn/large/006tKfTcgy1fhntdjsestj309z0dkq47.jpg)

- 更改工程签名

![](https://ws1.sinaimg.cn/large/006tKfTcgy1fhntdrd0kkj312w0q00xw.jpg)

- 运行你的工程
    - 此时你的iphone应该会提醒你该应用不被信任，无法运行
    - 进入iphone-设置-通用-描述文件与设备管理-允许你的开发者应用
- 再次运行你的工程
    - Disco！

