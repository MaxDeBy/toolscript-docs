[Back to overview](index.md)

---
# PlayMusic (PM)
---
### Description
Plays a music track.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Name|String|The name of the music track.|✓|-|

### Examples:
#### Example #1: Plays the music track 'Prelude'.
```
1:  PlayMusic:["Prelude"];
```

### Remarks:
Before playing a song, make sure the previous song was stopped with the [StopMusic](StopMusic.md) instruction.  
If you do not, it will most likely freeze the whole game for multiple seconds before playing the track. Why? Heck if I know.

---
[Back to overview](index.md)