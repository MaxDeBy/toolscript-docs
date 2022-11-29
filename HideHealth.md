[Back to overview](index.md)

---
# HideHealth (HH)
---
### Description
This instruction hides the health bar.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Mode|Boolean|Determines whether or not a sliding animation should be used.|✓|false|

### Examples:
#### Example #1: Hiding the health bar with a slide animation.
```
1:  HideHealth:[true];
```

#### Example #2: Hiding the health bar with no slide animation instruction.
```
1:  HH:[false];
```

### Remarks:
There are two health bars. The first is the regular health bar that is usually displayed during a trial and a second one for the psyche locks. The health bar is on the left side, as opposed to the psyche bar which is on the right side. There is also a special frame ID `GameOver` which you can give to a frame to mark it as a GameOver frame. A GameOver frame will be called if the health drops down to 0. Once the content of the GameOver frame has been executed, the game will automatically end.

The appearance and position of the healthbar can be modified via themes.

---
[Back to overview](index.md)