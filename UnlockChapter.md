[Back to overview](index.md)

---
# UnlockChapter (UC)
---
### Description
Unlocks a chapter, making it available from the chapter selection menu.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Chapter Number|Number|The number of the chapter.|✓|-|

### Examples:
#### Example #1: Unlock chapter 2.
```
1:  UnlockChapter:[2];
```

### Remarks:
All chapters except the chapter with the lowest number start out being locked by default.  
They are not being unlocked automatically, so you need to call this instruction in order to let the player progress.

---
[Back to overview](index.md)
