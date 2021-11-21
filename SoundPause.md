[Back to overview](index.md)

---
# SoundPause
---
### Description
A second way of pausing for a little. Instead of using miliseconds, you can input the name of a sound effect, and the engine will wait until the sound effect's full duration has passed before it proceeds.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Name|String|The name of the sound effect which's length should be waited for.|✓|-|

### Examples:
#### Example #1: Wait for the length of the 'Deskslam' sound effect.
```
1:  SoundPause:["Deskslam"];
```

### Remarks:
The engine will wait, regardless if the sound is actually played or not.  
Note that this can cause crashes if the sound file is not encoded properly. This is not a reliable way to wait for something to finish.  
Only use this Instruction if there is nothing visually to wait for. If you only need to wait for an animation to finish, use [DisplayPopupWait](DisplayPopupWait.md) or the `Wait for pre` parameter in the [LoadScene](LoadScene.md) Instruction.

---
[Back to overview](index.md)