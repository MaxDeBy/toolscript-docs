[Back to overview](index.md)

---
# ShowNoise (Noise)
---
### Description
Displays a noise animation for Mood Matrix.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Param Name|Number|The number the counter should start at.|✓|100|
|Param Name 2|Number|The number the counter should end at.|✗|0|

### Examples:
#### Example #1: Show a noise animation going from 10% to 80%.
```
1:  ShowNoise:[10|80];
```

#### Example #1: Show a noise animation going from 10% to 0%.
```
2:  Noise:[20];
```

### Remarks:
Depending on whether the start count is higher or lower than the end count, a different animation is played.

Also, if the end count is 0 then an ending animation will be played. This occurs only if the start is higher than 0.

The noise animation is not tied to a Mood Matrix sequence. It can be displayed at any time and has no impact on anything else.
It is a visual feature, not a functional one. 

---
[Back to overview](index.md)