[Back to overview](index.md)

---
# DecreaseHealth (Damage)
---
### Description
Reduces the amount of health left.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Amount|Number|The amount of health that should be removed.|✓|0|

### Examples:
#### Example #1: Taking 50 damage.
```
1:  ...
2:  DecreaseHealth:[50];
3:  ...
```

#### Example #1: Taking 20 damage.
```
1:  ...
2:  Damage:[20];
3:  ...
```

### Remarks:
The maximum amount of health is 100. 
The health bar will automatically be displayed when the health is changed, provided it wasn't already displayed

Should the health fall to 0 or below, a the Frame with the ID `GameOver` will be called, should it exist. Afterwards, the game will end.

---
[Back to overview](index.md)