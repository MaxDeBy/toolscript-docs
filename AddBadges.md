[Back to overview](index.md)

---
# AddBadges
---
### Description
Add a specified amount of badges to the badge healthbar.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Badges|Number|The amount of badges to add.|✓|1|

### Examples:
#### Example #1: Add 2 badges.
```
1:  Add:[2];
```

#### Example #2: Add 1 badge.
```
1:  Add:[-];
```

### Remarks:
The badge healthbar is independant from the regular healthbar and they can both be used in the same game without influencing each other. However, the badge healthbar is still a healthbar. This means, that if the last badge is [destroyed](DestroyBadges.md), 
the frame with the ID `GameOver` will be executed, if it exists.

The appearance and position of the healthbar can be modified via themes.

> The amount of initial badges can be set via themes by setting the `meta` attribute on the `BadgeHealthBar` element.

---
[Back to overview](index.md)