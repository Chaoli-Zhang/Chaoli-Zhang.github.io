---
layout:     post                                    # 使用的布局（不需要改）
title:      【小方法】无限期的免费使用付费软件（Mac）         # 标题
subtitle:   如何改变付费软件试用的天数            #副标题
date:       2017-10-28                              # 时间
author:     Chaoli Zhang                            # 作者
header-img: img/Tag-bg-hacker.jpg                  #这篇文章标题背景图片
catalog: true                                       # 是否归档
published: true
tags:                                               #标签
    - Code
    - Hack
---

如果你试用了某款好的软件，觉得很好，但是又不想买，那怎么样无限期的使用Trial版本的软件呢？
下面介绍一个用PlistEdit去修改试用期限的小方法。

好，废话少说，进入主题！

---
### 工具

你需要下载/安装以下的工具：

1. [PlistEdit Pro](https://www.fatcatsoftware.com/plisteditpro/)

### 方法
接下来我会用下面两款software来介绍这个工具的使用方法：

- [Bartender](https://www.macbartender.com/)
- [SteerMouse](http://plentycom.jp/en/steermouse/)

### 【[Bartender](https://www.macbartender.com/)】

Bartender可以把菜单栏应用程序移动到“酒保”那里，这样就看起来更干净整洁（处女座必备良器啊）。
下面是未试用Bartender的界面，是不是看上去很乱，

![bartender_1.png](/img/Free_app/bartender_1.png "bartender_1.png")

经过Bartender处理后的界面是这样的，是不是有心旷神怡的感觉：

![bartender_2.png](/img/Free_app/bartender_2.png "bartender_2.png")

下载安装Bartender之后会有35天的试用期，当35天过后，你可以用PlistEdit打开在`~/Library/Preferences/`目录下的`com.surteesstudios.Bartender.plist`文件，然后修改那个trialstart2的日期就可以了：

![bartender_3.png](/img/Free_app/bartender_3.png "bartender_3.png")

这样你一年只需要改12次就可以了完全免费试用这款software。（如果你觉得每个月都改太麻烦，那你可以写个shell script去自动化这个步骤）

### 【[SteerMouse](http://plentycom.jp/en/steermouse/)】

SteerMouse是一款让我们自由自定义鼠标的按键功能。

这款软件在`~/Library/Preferences/`也有相对应的`.plist`文件，但这个文件没有trialstart2这个选项。可能这款软件是日本人做的，所以他们比较介意别人用上面通过用PlistEdit去修改试用日期来达到延期的目的。

![steermouse_1.png](/img/Free_app/steermouse_1.png "steermouse_1.png")

那难道就没有办法了吗？我还是找到一个brutal force的办法，当你的试用期过了，可以试试下面的方法：

1. 先卸载SteerMouse的软件
2. 在terminal里面用`sudo find / -iname *SteerMouse*`找到所有和steermouse相关的文件
    - 这一步可能会费时一点，但是对于同一个软件里只需要搜索一次就足够，因为一旦搜索完成，你就把相应的文件及文件地址记录下来，然后写个shell script去自动完成。下面是我电脑找到所有和SteerMouse相关的文件：

```js
sudo rm -rf "/Library/PreferencePanes/SteerMouse.prefPane"
sudo rm -rf "/Library/PreferencePanes/SteerMouse.prefPane/Contents/MacOS/SteerMouse"
sudo rm -rf "/Library/PreferencePanes/SteerMouse.prefPane/Contents/MacOS/SteerMouse Manager.app"
sudo rm -rf "/Library/PreferencePanes/SteerMouse.prefPane/Contents/MacOS/SteerMouse Manager.app/Contents/MacOS/SteerMouse Manager"
sudo rm -rf "/Library/PreferencePanes/SteerMouse.prefPane/Contents/MacOS/SteerMouse Manager.app/Contents/Resources/SteerMouse.icns"
sudo rm -rf "/Library/PreferencePanes/SteerMouse.prefPane/Contents/Resources/SteerMouse.icns"
sudo rm -rf "/System/Library/Extensions/SteerMouse.kext"
sudo rm -rf "/System/Library/Extensions/SteerMouse.kext/Contents/MacOS/SteerMouse"
sudo rm -rf "/Users/ChaoliZhang/Library/Application Support/SteerMouse & CursorSense"

```
3. 删除在第二部找到的所有文件
4. 重新安装SteerMouse

这样你就可以重新使用了，等下次过期了，你可以重复上面的步骤，卸载，删除文件，然后重新安装即可。

---
---
### 总结

上面这2个只是例子，理论上你可以应用到其他的software（只要他们是有提供试用期）。当然，如果你有经济实力，那还是买下软件来用吧。毕竟人家程序员也是花了心血来写的软件。



