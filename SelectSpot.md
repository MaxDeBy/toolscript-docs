[Back to overview](index.md)

---
# Instruction Name (optional: Abbreviation)
---
### Description
General description of the instruction's purpose.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|X Pos|String|The position on the x-axis.|✓|-|
|Y Pos|Number|The position on the y-axis.|✓|-|
|Offset|Boolean|The offset around the x and y positions.|✓|-|
|Correct Frame|Boolean|The ID of the frame that should be played when the spot is clicked.|✓|-|
|Wrong Frame|Boolean|The ID of the frame that should be played when the wrong spot is clicked.|✓|-|

> Note: There will never be a parameter with the type `undefined`.

### Examples:
#### Example #1: Prompt the player to click a spot on (20,30) with an offset of 10 pixels. If the player clicks on that spot, frame '2' will be played. Otherwise frame '3' will be played.
```
1:  SelectSpot:[20|30|10|2|3];
```

### Remarks:
-

---
[Back to overview](index.md)