# Set up menstrual cycle reminders
### Function table
```objc
__IDO_FUNCTABLE__.funcTable20Model.menstruation
```
### Menstrual cycle reminder model description

* IDOSetMenstruationRemindBluetoothModel

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
<td>startDay</td>
<td>Start day reminder</td>
<td>Days in advance</td>
</tr>
<tr>
<td>ovulationDay</td>
<td>Ovulation day reminder</td>
<td>Days in advance</td>
</tr>
<tr>
<td>hour</td>
<td>Reminder time (Hour)</td>
<td>int</td>
</tr>
<tr>
<td>minute</td>
<td>Reminder time (Minute)</td>
<td>int</td>
</tr>
<tr>
<td>pregnancyDayBeforeRemind</td>
<td>How many days in advance to remind when the fertile period starts</td>
<td>int</td>
</tr>
<tr>
<td>pregnancyDayEndRemind</td>
<td>How many days in advance to remind when the fertile period is over</td>
<td>int</td>
</tr>
<tr>
<td>menstrualDayEndRemind</td>
<td>How many days in advance to remind when your period ends</td>
<td>int</td>
</tr>
</tbody>
</table>



### Command code

Objc:

```objc
IDOSetMenstruationRemindBluetoothModel * model = [IDOSetMenstruationRemindBluetoothModel currentModel];
[IDOFoundationCommand setMenstrualRemindCommand:model
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
let model = IDOSetMenstruationRemindBluetoothModel.current();
IDOFoundationCommand.setMenstrualRemind(model) { (errorCode) in
     if errorCode == 0 {
        //Set successfully
     }else if errorCode == 6{
        //Device does not support this method
     }else {
       //Wrong setting
     }
};
```
