

### 今日人品
**今日人品是根据各位的uid、日期等在一天当中不变的常量计算得出的随机数，并不会对各位的游戏体验、鱼子酱的使用产生影响。**

提示：在2021.4.15日后，今日人品的刷新时间已改为每日凌晨四点

```python
import datetime
import hashlib

def hex2dec(string_num):
    return str(int(string_num.upper(), 16))

def jrrp(id ,min ,max ,seed):

    today = datetime.date.today()
    year = str(today.year)
    month = str(today.month)
    day = str(today.day)

    md5 = str(id) + year + month + day
    md5 = str(md5) + str(seed)
    md5 = md5.encode('utf-8')
    m = hashlib.md5()
    m.update(md5)
    md5 = m.hexdigest()
    md5 = hex2dec(md5[-8:])
    result = int(md5) % (max - (min) + 1) + (min)
    return result
```

**指令：** `今日人品`

* 鱼子酱会对发送指令者进行顺序排名，快来看看大家今天都是第几个签到的吧

* 问候语现在会根据当前时间进行调整

* 按照人品数值大小可分为[大吉大利]、[大吉]、[中吉]、[小吉]、[末吉]、[凶]五个等级。

* 当人品处于区间21-99时鱼子酱会发送[随机一言](https://hitokoto.cn/)

* 当人品处于2-20时鱼子酱会发送[毒鸡汤](https://github.com/egotong/nows)

> 没事打开http://www.nows.fun/ 毕竟人生苦短都没苦笑过有什么意思！



**指令：** `塔罗牌抽取`

* 来抽随机抽一张塔罗牌吧

***
### Wordscloud词云
**词云功能会自动将消息记录中的句子拆分统计为词语并统计次数，收到指令后会生成一张与词频有关的图片**

**插件开源地址：[OlivaWordCloud](https://github.com/Fishroud/OlivaWordCloud)**

**指令：**：`wordcloud`

***
### 更改鱼子酱对自己的称呼
**自定义鱼子酱对你的称呼，不需要添加中括号，长度限制为20个字节。默认调用QQ昵称，以后的更多功能或许会用到**

**指令：**：`鱼子酱，叫我[自定义昵称]`

***

### 快速反馈意见

**使用指令`鱼子酱，反馈[bug反馈及建议]`可快速向维护者反馈建议，不需要添加中括号，请勿滥用**

***



### 鱼子酱贴心提醒功能（正在维护）

**在群聊中向鱼子酱添加对指定用户的提醒消息后，鱼子酱将会在该用户下次发言时发送你所提交的提醒信息**

**指令:** `提醒@某人 某事`

将提醒信息添加到鱼子酱，请注意：

* 无法提醒自己和鱼子酱
* 由于风险控制考虑，请勿提交过长的提醒内容

**正确示例：**  
指令： `提醒@鱼仙 来打彩虹六号`

当鱼仙下次发言时推送：
```
@鱼仙
在你不在的时间里，你收到了1条提醒
1.2021-04-07 22:00:42
来自xxxxxxx：来打彩虹六号
```

***

### Todo：
#### 代码PHP + 数据库重构
* steam相关功能 √
* bilibili监控功能 √
* 好感度功能 
* 坦克世界查询功能 √

#### 鱼子酱互动功能
* 互动指令与好感度等级回复 √
* 对于特定好感度下的专属回复 √

#### war of warship
* 模糊id搜索绑定 √
* 战绩查询 

**资料来源：[Wargaming Api Reference](https://developers.wargaming.net/reference/all/wot/account/list/?r_realm=ru)**