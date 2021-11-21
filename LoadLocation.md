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

### Examples:
#### Example #1: Loading the 'Agency' background.
```
1:  LoadLocation:["Agency"];
```

### Remarks:
Super locations are locations that extent beyond the screen dimensions, on both the X and the Y axis. Background and/or foreground image can be bigger than the screensize and will be displayed without resizing.  
Characters can be set on any position, regardless if the current location is a super location or not. See more under [LoadCharacter](LoadCharacter.md).
 
Just like its predecessor **LoadScene**, this instruction will remove the popup, dialog box and all characters from the screen.

---
[Back to overview](index.md)