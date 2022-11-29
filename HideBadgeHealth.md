[Back to overview](index.md)

---
# HideBadgeHealth (HBH)
---
### Description
This instruction hides the badge healthbar.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Mode|Boolean|Whether the badge healthbar should slide out of view or disappear instantly.|✓|false|

### Examples:
#### Example #1: Hiding the health bar with a slide animation.
```
1:  HideBadgeHealth:[true];
```

#### Example #2: Hiding the health bar with no slide animation instruction.
```
1:  HBH:[false];
```

### Remarks:
The badge healthbar is independant from the regular healthbar and they can both be used in the same game without influencing each other. However, the badge healthbar is still a healthbar. This means, that if the last badge is [destroyed](DestroyBadges.md),
the frame with the ID `GameOver` will be executed, if it exists.

The appearance and position of the healthbar can be modified via themes.

---
[Back to overview](index.md)