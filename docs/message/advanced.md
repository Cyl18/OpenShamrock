---
title: 高级消息
icon: layer-group
---

::: warning 注意
对于 Shamrock 未实现的消息类型，会在标题添加标记 <Badge text="未实现" type="danger" vertical="baseline" />
:::

## 合并转发

| 字段 | 类型   | 收  | 发  | 必填 | 说明          |
| ---- | ------ | --- | --- | ---- | ------------- |
| id   | string | ✓   | ✓   | 是   | 合并转发resid |

## 合并转发(节点)

| 字段 | 类型  | 收  | 发  | 必填 | 说明   |
| ---- | ----- | --- | --- | ---- | ------ |
| id   | `int64` or `string` | ✓   | ✓   | 是   | 消息ID |

## XML 消息 <Badge text="未实现" type="danger" />

## JSON 消息

### 参数

| 字段 | 类型   | 收  | 发  | 必填 | 说明      |
| ---- | ------ | --- | --- | ---- | --------- |
| data | string | ✓   | ✓   | 是   | JSON 数据 |

::: tabs

@tab CQ 码

```text
[CQ:json,data={"app":"com.tencent.structmsg","config":{"autosize":true,"ctime":1621234567,"forward":true,"token":"shamrock"},"desc":"这是一条 JSON 消息"...}]
```

@tab 消息段

```json
{
  "type": "json",
  "data": {
    "data": "{\"app\":\"com.tencent.structmsg\",\"config\":{\"autosize\":true,\"ctime\":1621234567,\"forward\":true,\"token\":\"shamrock\"},\"desc\":\"这是一条 JSON 消息\"...}"
  }
}
```

:::

## 文本转语音 <Badge text="未实现" type="danger" />
