## bilibili相关功能
***
### bilibili链接解析

**插件开源地址：[OlivaBilibiliPlugin](https://github.com/Fishroud/OlivaBilibiliPlugin)**

从现在开始，鱼子酱将自动解析发送到群内的如下内容

* AV号
* BV号
* btv短链接
* 直播间链接

详情请参阅[bilibili-API-collect](https://github.com/SocialSisterYi/bilibili-API-collect)

av,bv,btv链接相关内容会被解析并以如下格式发出

```
[AV\BV号]
[视频封面图片]
[视频标题]
[up主][mid]
[视频简介]
[在线观看人数]
[播放数量]
[视频链接]
```



**示例：**  
指令：
* `BV1uQ4y1y76v`
* `https://www.bilibili.com/video/BV1uQ4y1y76v`


返回:
```
[BV1uQ4y1y76v]
[这里是封面图]
标题：【雨宮みお】狐狐の普罗万伤百轻
up主：雨宮みおoffical[7213878]
简介：少见的普罗万伤，在这之中其实还有非常多地方的不足，本来可以不用拖到平局，因为自己犹豫了一下便等到最后两分钟才去侦查，可以的话麻烦一键三连点个关注，可以的话也请点个关注，谢谢~ (＾▽＾)
在线观看人数：1
播放数量：373
链接：https://www.bilibili.com/video/BV1uQ4y1y76v
```

***

直播间链接相关内容会被解析并以如下格式发出

```
鱼子酱发现了bilibili直播房间链接！
该主播当前正在/未在直播
开播时间：yyyy-mm-dd hh:mm:ss
[up主][mid]
[直播间链接]
[直播间标题]
[直播间封面图]
```

**示例：**  
指令：
* `https://live.bilibili.com/1004185`


返回:
```
鱼子酱发现了bilibili直播房间链接！
该主播当前未在直播
雨宮みおoffical[7213878]
https://live.bilibili.com/1004185
标题：【战争雷霆】菜狐桑德Time
[这里是直播间封面图]
```



### bilibili直播监控

**本功能暂未开放，如需使用请加入鱼子酱加工厂申请**

鱼子酱将会对特定的up主直播间进行监控，并在开播时推送到指定群聊
 

```
收到来自后端服务器的直播推送
群关注的up主院长[862684]开播啦！
标题:【战争雷霆】老年人复健
开播时间:2021-04-07 18:39:30
链接:https://live.bilibili.com/5991000
[直播间封面]
[直播关键帧]
```

