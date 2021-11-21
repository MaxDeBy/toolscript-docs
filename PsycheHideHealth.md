[Back to overview](index.md)

---
# PsycheHideHealth (PsyHH)
---
### Description
Hides the psyche bar.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Slide|Boolean|Determines whether the psyche bar should disappear with a slide animation.|✓|false|

### Examples:
#### Example #1: Hides the psyche health bar with a sliding animation.
```
1:  PsycheHideHealth:[true];
```

#### Example #2: Hides the psyche health bar without a sliding animation.
```
1:  PsyHH:[false];
```

### Remarks:
There are two health bars. The first is the regular health bar that is usually displayed during a trial and a second one for the psyche locks. The second bar is refered to as "psyche bar" in AACT. The psyche bar is on the right side, as opposed to the normal health bar which is on the left side. It supports the same features as the regular health bar. There is also a special frame ID `PsycheOver` which is just like the `GameOver` frame ID. While the GameOver frame automatically ends the game, the PsycheOver frame does not, so it can be used multiple times.

---
[Back to overview](index.md)