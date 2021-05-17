[Back to overview](index.md)

---
# FadeOutScene
---
- **Name:** FadeOutScene (FoutScene)
- **Description:** Fades the screen (meaning, character, foreground AND background) to black.
- **Parameters:**
  - **Delay:**  
    The amount of miliseconds it takes to fade out the scene.

- Examples:
```
1:  FadeOutScene:[1000];
2:  FoutScene:[-];
```

- Remarks:
> If you pass an empty parameter as delay, it will default to one second (1000 miliseconds).  
The minimum is 10 miliseconds. If you use a value lower than 10, it will be considered as 10. The only exception is 0 miliseconds, which are treated as instantly.

---
[Back to overview](index.md)