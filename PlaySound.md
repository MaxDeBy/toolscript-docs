[Back to overview](index.md)

---
# PlaySound (PS)
---
### Description
This instruction plays a sound effect.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Name|String|The name of the sound effect.|✓|-|
|Delay|Number|Waits this amount of miliseconds before actually playing the sound.|✗|0|
|Loop|Boolean|Determines whether the sound should loop or not.|✗|false|

### Examples:
#### Example #1: Plays the sound 'GavelSlam' in 300ms.
```
1:  PS:["GavelSlam"|300];
```

#### Example #2: Plays the sound 'Clap' immediately and loop until stopped manually.
```
1:  PlaySound:["Clap"|0|true];
```

#### Example #3: Play the sound 'Chalkboard' immediately.
```
1:  PS:["Chalkboard"];
```

### Remarks:
If `Delay` is set to anything below 10, it will be interpreted as 10. The only exception is the value 0.

---
[Back to overview](index.md)