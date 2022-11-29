[Back to overview](index.md)

---
# DestroyBadges
---
### Description
Destroy a specified amount of badges.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Badges|Number|The amount of badges to destroy.|✓|1|

### Examples:
#### Example #1: Destroy 2 badges.
```
1:  DestroyBadges:[2];
```

#### Example #2: Destroy 1 badge.
```
1:  DestroyBadges:[-];
```

### Remarks:
The badge healthbar is independant from the regular healthbar and they can both be used in the same game without influencing each other. However, the badge healthbar is still a healthbar. This means, that if the last badge is destroyed, 
the frame with the ID `GameOver` will be executed, if it exists.

The appearance and position of the healthbar can be modified via themes.

---
[Back to overview](index.md)