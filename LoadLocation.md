[Back to overview](index.md)

---
# LoadLocation (LL)
---
### Description
Loads a location or super location, replacing the previous location.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Name|String|The name of the location.|✓|-|
|PosX|Number|The start position of the camera on the X axis.|✗|0|
|PosY|Number|The start position of the camera on the Y axis.|✗|0|

### Examples:
#### Example #1: Loading the 'Agency' background.
```
1:  LoadLocation:["Agency"];
```

#### Example #1: Loading the 'Agency' background and instantly snap the camera to a (X:920,Y:384).
```
1:  LoadLocation:["Agency"|920|384];
```

### Remarks:
Super locations are locations that extent beyond the screen dimensions, on both the X and the Y axis. Background and/or foreground image can be bigger than the screensize and will be displayed without resizing.  
Characters can be set on any position, regardless if the current location is a super location or not. See more under [LoadCharacter](LoadCharacter.md).
 
Just like its predecessor **LoadScene**, this instruction will remove the popup, dialog box and all characters from the screen.

---
[Back to overview](index.md)