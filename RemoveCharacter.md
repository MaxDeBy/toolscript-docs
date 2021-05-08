[Back to overview](index.md)

---
# RemoveCharacter
---
- Name: RemoveCharacter (Snap)
- Description: Removes a character from the screen.
- Parameters
  - **Character Position:**  
    The position of the character that is supposed to be removed.

- Examples:
```
1:  RemoveCharacter:["Center"];
2:  Snap:["All"];
```

- Remarks
> There are 3 character positions: `Right`, `Left` and `Center`.  
Although, they can be combined. Valid position combinations are: `RightLeft`, `RightCenter`, `LeftCenter` and `All`.
> 
> This counts for all instructions that use character positions. When omitted or invalid, the default value is `Center`.

---
[Back to overview](index.md)