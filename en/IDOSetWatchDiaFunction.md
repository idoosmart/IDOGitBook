# Set the watch face ID

### Dial ID Model Description

* IDOSetWatchDiaInfoBluetoothModel

<table border="1px" width="100%">
<thead>
<tr>
<th><strong>Parameters</strong></th>
<th><strong>Description</strong></th>
<th><strong>Notes</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>dialId</td>
<td>Watch face ID</td>
<td>int</td>
</tr>
</tbody>
</table>


### command code

Objc:

```objc
IDOSetWatchDiaInfoBluetoothModel * model = [IDOSetWatchDiaInfoBluetoothModel currentModel];
[IDOFoundationCommand setWatchDiaCommand:model
                                callback:^(int errorCode) {
    if (errorCode == 0) {
       //set successfully
     }else if (errorCode == 6) {
       //The device does not support
     }else {
       //Setup failed
    }
}];
```

Swift:

```swift
let model = IDOSetWatchDiaInfoBluetoothModel.current();
IDOFoundationCommand.setWatchDia(model) { (errorCode) in
     if errorCode == 0 {
        //set successfully
      }else if errorCode == 6{
         //The device does not support this method
      }else {
        // set error
     }
};
```
