[Back to overview](index.md)

---
# MoveCharacter (MoveChar)
---
### Description
Moves a character to a different position.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Position X|Number|The destination position of the character on the X axis of the background image. The value describes the leftmost pixel which should be visible.|✓|-|
|Position Y|Number|The destination position of the character on the Y axis of the background image. The value describes the topmost pixel which should be visible.|✗|0|
|Duration|Number|The time in miliseconds the moving should take. 0 being instantly.|✗|0|
|Wait|Boolean|Whether or not the engine should wait until the moving has been completed before continuing.|✗|false|

### Examples:
#### Example #1: Moving a character instantly to pixel 1280 on the X-axis.
```
1:  ...
2:  MoveCharacter:[1280];
3:  ...
```

#### Example #2: Moving a character to position (1200,400) with a transition duration of 2 seconds. AACT waits for the moving to be completed before moving on.
```
1:  ...
2:  MoveChar:[1200|400|2000|true];
3:  ...
```

### Remarks:
-

---
[Back to overview](index.md)