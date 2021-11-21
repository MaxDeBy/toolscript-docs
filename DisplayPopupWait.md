[Back to overview](index.md)

---
# DisplayPopupWait (DPW)
---
### Description
Displays a popup animation and waits until the animation has finished playing.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Popup name|String|The name of the popup that should be displayed.|✓|-|

### Examples:
#### Example #1: Displaying the objection bubble popup paired with a sound and wait for it to finish.
```
1:  ...
2:  PlaySound:["PW-Objection"];
3:  DisplayPopupWait:["Objection"];
4:  ...
```

### Remarks:
The popup will not vanish until [LoadLocation](LoadLocation.md) has been called.  
This Instruction does not support looping, for obvious reasons. If you need a looping popup, use [DisplayPopup](DisplayPopup.md) instead.

---
[Back to overview](index.md)