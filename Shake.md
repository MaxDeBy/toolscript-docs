[Back to overview](index.md)

---
# Shake
---
### Description
Shakes the screen with a specified intensity and duration.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Intensity|Number|The intensity of the shaking. Must be a value between 0-255.|✗|10|
|Duration|Number|The duration of the shaking in miliseconds. Must be a value between 10-65535.|✗|200|

### Examples:
#### Example #1: Shaking the camera with an intensity of 20 for 200 miliseconds.
```
1:  ...
2:  Shake:[20];
3:  ...
```

#### Example #2: Shaking the camera with an intensity of 30 for 5 seconds.
```
1:  ...
2:  Shake:[30|5000];
3:  ...
```

### Remarks:
Shaking effect is only applied to the camera layer. Every other layer remains still during a shake effect.
Shaking is an asynchronous effect, meaning the engine will not wait for it to finish before continuing.
 
Since AACT is a 2D engine, a "camera" in traditional sense does not exist. Instead, camera here refers to an element that will affect its children. The children can be configured via themes.
Only those children will be affected by this instruction.

---
[Back to overview](index.md)