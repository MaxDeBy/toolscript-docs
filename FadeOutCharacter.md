[Back to overview](index.md)

---
# FadeOutCharacter
---
- **Name:** FadeOutCharacter (FoutChar)
- **Description:** Fades out the character of the screen.
- **Parameters:**
  - **Delay:**  
    The amount of miliseconds it takes to fade out the character.
  - **Character position (optional):**  
    The position of the character that is supposed to fade out
 
- Examples:
```
1:  FadeOutCharacter:[1000];
2:  FoutChar:[-];
3:  FadeOutCharacter:[1000|"RightLeft"];
4:  FoutChar:[-|"RightLeft"];
```

- Remarks:
> If you pass an empty parameter as delay, it will default to one second (1000 miliseconds).  
The minimum is 10 miliseconds. If you use a value lower than 10, it will be considered as 10. The only exception is 0 miliseconds, which are treated as instantly.
> 
> There are 3 character positions: `Right`, `Left` and `Center`.  
> Although, they can be combined. Valid position combinations are: `RightLeft`, `RightCenter`, `LeftCenter` and `All`.
> 
> This counts for all instructions that use character positions. When omitted or invalid, the default value is `Center`.

---
[Back to overview](index.md)