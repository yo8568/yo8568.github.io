---
layout: post
title: 在Linux中查詢本機對外IP
categories:
  - work-tips
tags:
  - Linux
  - tips
---

### 工作指令小記 - 在Linux中查詢本機對外IP

一個突然，都會忘記linux指令

大家應該都知道 ifconfig 可以看有關網路的參數

```
ifconfig {interface} {up|down}   // 觀察與啟動介面
ifconfig interface {options}     // 設定與修改介面

選項與參數：
interface：網路卡介面代號，包括 eth0, eth1, ppp0 等等
options  ：可以接的參數，包括如下：
    up, down ：啟動 (up) 或關閉 (down) 該網路介面(不涉及任何參數)
    mtu      ：可以設定不同的 MTU 數值，例如 mtu 1500 (單位為 byte)
    netmask  ：就是子遮罩網路；
    broadcast：就是廣播位址啊！
```

但是，突然要查外部IP，就會有點傻眼
登登～～～   這個就可以找到囉～～～

> curl ifconfig.me

其實ifconfig.me是一個網站

如果你開瀏覽器輸入網址 [http://ifconfig.me](http://ifconfig.me)

就會顯示你的外部ip，而且還多了各樣資訊出來，嚇死寶寶了！