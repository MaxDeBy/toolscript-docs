[Back to overview](index.md)

---
# PanCamera (Cam)
---
### Description
Pans the camera to a different spot of the current super location.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Position X|Number|The destination position of the camera on the X axis of the background image. The value describes the leftmost pixel which should be visible.|✓|-|
|Position Y|Number|The destination position of the camera on the Y axis of the background image. The value describes the topmost pixel which should be visible.|✗|0|
|Duration|Number|The time in miliseconds the panning should take. 0 being instantly.|✗|0|
|Linear|Boolean|Whether the panning should occurr with a consistent speed or ease in and out.|✗|false|
|Wait|Boolean|Whether or not the engine should wait until the panning has been completed before continuing.|✗|false|

### Examples:
#### Example #1: Moving the camera instantly to pixel 1280 on the X-axis.
```
1:  ...
2:  Cam:[1280];
3:  ...
```

#### Example #2: Panning the camera to position (1200,400) with a transition duration of 2 seconds. The camera does not ease in or out and AACT waits for the panning to be completed before moving on.
```
1:  ...
2:  PanCamera:[1200|400|2000|true|true];
3:  ...
```

### Remarks:
Super locations are locations that extent beyond the screen dimensions, on both the X and the Y axis. Background and/or foreground image can be bigger than the screensize and will be displayed without resizing.  
Characters can be set on any position, regardless if the current location is a super location or not. See more under [LoadCharacter](LoadCharacter.md).
 
Since AACT is a 2D engine, a "camera" in traditional sense does not exist. Instead, camera here refers to an element that will affect its children. The children can be configured via themes. This instruction, however, is independant from the setup in themes.

This instruction fades out the dialog box before starting the panning.

This instruction will automatically move all characters on the screen as well.

---
[Back to overview](index.md)