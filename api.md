## 鱼子酱扩展api文档
***
### 鱼子酱毒鸡汤

**GET** 
`http://api.fishroud.xyz/`

**响应数据**

| 字段 | 类型 | 说明 |
| :----:| :----:|:----:|
| `title` | string | 标题 |
| `request` | string | 若访问成功则为success |
| `msg` | string | 毒鸡汤 |


```json
{
  "title": "鱼仙牌毒鸡汤",
  "request": "success",
  "msg": "听说你过的不好，我蹲在门口，笑了一整天。"
}
```
***
### 舟游圣经

**GET** 
`http://api.fishroud.xyz/arknights.php`


**响应数据**

| 字段 | 类型 | 说明 |
| :----:| :----:|:----:|
| `request` | string | 若访问成功则为success |
| `title` | string | 标题|
| `id` | int | 条目号 |
| `msg` | string | 舟游圣经 |
| `length` | int | msg长度 |


```json
{
  "request": "success",
  "title": "方舟圣经",
  "id": 1,
  "msg": "为斯卡蒂献上心脏！！！",
  "length": 11
}
```

***
### 落落的诗

**GET** 
`http://api.fishroud.xyz/poem.php`

**响应数据**

| 字段 | 类型 | 说明 |
| :----:| :----:|:----:|
| `request` | string | 若访问成功则为success |
| `title` | string | 标题|
| `id` | int | 条目号 |
| `msg` | string | 随机一句诗 |


```json
{
  "request": "success",
  "title": "落落的诗",
  "id": 128,
  "msg": "想念的人\\n先说想你\\n像咬破一颗果实\\n反倒是汁水进攻了嘴巴"
}
```