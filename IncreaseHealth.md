[Back to overview](index.md)

---
# IncreaseHealth (Heal)
---
### Description
Increases the amount of health.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Amount|Number|The amount of health to add.|✓|-|

### Examples:
#### Example #1: Increasing the current health by 20.
```
1:  IncreaseHealth:[20];
```
#### Example #2: Increasing the current health by 50.
```
2:  Heal:[50];
```
### Remarks:
The maximum amount of health is 100. 
The health bar will automatically be displayed when the health is changed, provided it wasn't already displayed.  

Should the health fall to 0 or below, a the Frame with the ID `GameOver` will be called, should it exist. Afterwards, the game will end.

---
[Back to overview](index.md)