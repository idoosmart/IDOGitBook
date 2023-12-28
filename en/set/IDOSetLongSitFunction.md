# Set a sedentary reminder
### Function table
```objc
__IDO_FUNCTABLE__.funcTable11Model.sedentariness
```
### Sedentary Model Instructions

* IDOSetLongSitInfoBuletoothModel

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
<td>startHour</td>
<td>Start (Hour)</td>
<td>int</td>
</tr>
<tr>
<td>startMinute</td>
<td>Start (Minute)</td>
<td>int</td>
</tr>
<tr>
<td>endHour</td>
<td>Finish (Hour)</td>
<td>int</td>
</tr>
<tr>
<td>endMinute</td>
<td>Finish (Minute)</td>
<td>int</td>
</tr>
<tr>
<td>interval</td>
<td>Interval</td>
<td>0-10 minutes</td>
</tr>
<tr>
<td>isOpen</td>
<td>Switch</td>
<td>bool</td>
</tr>
<tr>
<td>selectWeeks</td>
<td>Repeat set</td>
<td>[Monday,Tuesday,Wednesday,Thursday,Friday,Saturday,Sunday]</td>
</tr>
</tbody>
</table>


### Command code

Objc:

```objc
IDOSetLongSitInfoBuletoothModel * model = [IDOSetLongSitInfoBuletoothModel currentModel];
[IDOFoundationCommand setLongSitCommand:model
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
let model = IDOSetLongSitInfoBuletoothModel.current();
IDOFoundationCommand.setLongSit(model) { (errorCode) in
     if errorCode == 0 {
        //Set successfully
     }else if errorCode == 6{
        //Device does not support this method
     }else {
       //Wrong setting
     }       
};
```
