[Back to overview](index.md)

---
# DisplayPopup (DP)
---
### Description
Displays a popup animation.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Popup name|String|The name of the popup that should be displayed.|✓|-|
|Looping|Boolean|Determines whether the popup should loop or not.|✗|false|

### Examples:
#### Example #1: Displaying the 'Hold It!' bubble animation.
```
1:  DisplayPopup:["HoldIt"];
```

#### Example #2: Displaying the 'Testimony' indicator and make it loop.
```
1:  DP:["Testimony"|true];
```

### Remarks:
The popup will not vanish until LoadLocation has been called.

---
[Back to overview](index.md)