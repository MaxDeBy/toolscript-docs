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
|Loop|Boolean|Whether the sound should loop or not.|✗|false|
|Loop Delay|Number|The delay in miliseconds after each loop before the sound plays again. Does nothing if Loop is false.|✗|false|

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

#### Example #2: Plays the sound 'Clap' after 200 miliseconds and loop until stopped manually, waiting one second after each loop before playing again.
```
1:  PlaySound:["Clap"|200|true|1000];
```

### Remarks:
If `Delay` or `LoopDelay` is set to anything below 10, it will be interpreted as 10. The only exception is the value 0.

---
[Back to overview](index.md)