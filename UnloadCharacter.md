[Back to overview](index.md)

---
# UnloadCharacter (Snap)
---
### Description
Removes a character from the screen.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Position|String|The position of the character that's supposed to be removed.|✓|"Center"|

### Examples:
#### Example #1: Remove the character spot 'Defense'.
```
1:  Snap:["Defense"];
```

### Remarks:
The character position is the name given when the character was [loaded](LoadCharacter.md). 
This counts for all instructions that use character positions. When omitted or invalid, the default value is `Center`.

This instruction was called RemoveCharacter before 2.0.8. It has been renamed for the sake of consistency.

---
[Back to overview](index.md)