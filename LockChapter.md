[Back to overview](index.md)

---
# LockChapter (LC)
---
### Description
Locks a chapter, making it unavailable from the chapter selection menu.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Chapter Number|Number|The number of the chapter.|✓|-|

### Examples:
#### Example #1: Locking chapter 4.
```
1:  LockChapter:[4];
```

### Remarks:
All chapters except the chapter with the lowest number start out being locked by default.
Thus, this instruction is only required if you need to relock a chapter for whatever reason.

---
[Back to overview](index.md)
