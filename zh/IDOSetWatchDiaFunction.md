# 设置表盘ID

### 表盘ID模型说明

* IDOSetWatchDiaInfoBluetoothModel

<table border="1px" width="100%">
<thead>
<tr>
<th><strong>参数</strong></th>
<th><strong>说明</strong></th>
<th><strong>备注</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>dialId</td>
<td>表盘ID</td>
<td>int</td>
</tr>
</tbody>
</table>

### 命令代码

Objc:

```objc
IDOSetWatchDiaInfoBluetoothModel * model = [IDOSetWatchDiaInfoBluetoothModel currentModel];
[IDOFoundationCommand setWatchDiaCommand:model
                                callback:^(int errorCode) {
    if (errorCode == 0) {
       //设置成功
    }else if (errorCode == 6) {
      //设备不支持
    }else {
      //设置失败
    }
}];
```

Swift:

```swift
let model = IDOSetWatchDiaInfoBluetoothModel.current();
IDOFoundationCommand.setWatchDia(model) { (errorCode) in
     if errorCode == 0 {
        //设置成功
     }else if errorCode == 6{
        //设备不支持此方法
     }else {
       //设置错误
     }
};
```
