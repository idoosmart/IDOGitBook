
#### 设备发送交换运动数据结束命令


**App收到的json字段**：

| 字段名 | 字段类型 | 字段说明    |
| ------ | -------- | ----------- |
| day    | int      | 结束时间 日 |
| hour   | int      | 结束时间 时 |
| minute | int      | 结束时间 分 |
| second | int      | 结束时间 秒 |

`示例：`

```c
{
    "day":26,
    "hour":11,
    "minute":3,
    "second":15
}
```

**App下发的json字段**:

| 字段名   | 字段类型 | 字段说明                                   |
| -------- | -------- | ------------------------------------------ |
| ret_code | int      | 0：成功<br />1：没有进入运动模式失败 |

`示例：`

```c
{
    "ret_code":0
}
```