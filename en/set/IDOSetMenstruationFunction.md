# Set up a menstrual cycle

### Description of the physiological cycle model

* IDOSetMenstruationInfoBluetoothModel

<table border="1px" width="100%">
<thead>
<tr>
<th><strong>Parameter</strong></th>
<th><strong>Description</strong></th>
<th><strong>Remark</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>onOff</td>
<td>Switch</td>
<td>bool</td>
</tr>
<tr>
<td>menstrualLength</td>
<td>Menstrual Length</td>
<td>int</td>
</tr>
<tr>
<td>MenstrualCycle</td>
<td>Menstrual cycle</td>
<td>int</td>
</tr>
<tr>
<td>lastMenstrualYear</td>
<td>Year of last menstrual period</td>
<td>int</td>
</tr>
<tr>
<td>lastMenstrualMonth</td>
<td>Month of last menstrual period</td>
<td>int</td>
</tr>
<tr>
<td>lastMenstrualDay</td>
<td>Day of last menstrual period</td>
<td>int</td>
</tr>
<tr>
<td>ovulationIntervalDay</td>
<td>The interval between ovulation days</td>
<td>int</td>
</tr>
<tr>
<td>ovulationBeforeDay</td>
<td>Day before period</td>
<td>int</td>
</tr>
<tr>
<td>ovulationAfterDay</td>
<td>Day after period</td>
<td>int</td>
</tr>
<tr>
<td>notifyFlag</td>
<td>Notification type</td>
<td>0 Invalid ； 1：Allow notifications； 2：Silent notification； 3：Turn off notifications</td>
</tr>
</tbody>
</table>



### Command code

Objc:

```objc
IDOSetMenstruationInfoBluetoothModel * model = [IDOSetMenstruationInfoBluetoothModel currentModel];
[IDOFoundationCommand setMenstrualCommand:model
                                callback:^(int errorCode) {
    if (errorCode == 0) {
       //Set successfully
    }else if (errorCode == 6) {
      //Device not supported
    }else {
      //Setup failed
    }
}];
```

Swift:

```swift
let model = IDOSetMenstruationInfoBluetoothModel.current();
IDOFoundationCommand.setMenstrual(model) { (errorCode) in
     if errorCode == 0 {
        //Set successfully
     }else if errorCode == 6{
        //Device does not support this method
     }else {
       //Wrong setting
     }
};
```
