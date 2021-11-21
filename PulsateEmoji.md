[Back to overview](index.md)

---
# PulsateEmoji (Pulsate)
---
### Description
Makes an emoji pulsate during a Mood Matrix sequence.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Emoji|String|Does a thing.|✓|-|
|Diameter|Number|Specifies the diameter of the pulsation. A value of 0 stops the pulse.|✓|-|

### Examples:
#### Example #1: Pulsate the 'Happy' emoji with a diameter of 30 pixels.
```
1:  PulsateEmoji:["Happy"|20];
```

#### Example #2: Stops the 'Sad' emoji from pulsating.
```
1:  Pulsate:["Sad"|0];
```

### Remarks:
-

---
[Back to overview](index.md)