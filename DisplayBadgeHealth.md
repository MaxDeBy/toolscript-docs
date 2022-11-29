[Back to overview](index.md)

---
# DisplayBadgeHealth (DBH)
---
### Description
Displays the badge health bar.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Slide|Boolean|Whether the badge health bar should slide into view or appear instantly.|✗|false|

### Examples:
#### Example #1: Display the health bar with a sliding animation.
```
1:  DisplayBadgeHealth:[true];
```

#### Example #2: Display the healt hbar instantly.
```
1:  DBH:[false];
```

### Remarks:
The badge healthbar is independant from the regular healthbar and they can both be used in the same game without influencing each other. However, the badge healthbar is still a healthbar. This means, that if the last badge is [destroyed](DestroyBadges.md),
the frame with the ID `GameOver` will be executed, if it exists.

The appearance and position of the healthbar can be modified via themes.

---
[Back to overview](index.md)