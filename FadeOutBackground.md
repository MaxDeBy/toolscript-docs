[Back to overview](index.md)

---
# FadeOutBackground
---
- **Name:** FadeOutBackground (FoutBg)
- **Description:** Fades out the background of the screen.
- **Parameters:**
  - **Delay**:  
    The amount of miliseconds it takes to fade out the background.

- Examples:
```
1:  FadeOutBackground:[1000];
2:  FoutBg:[-];
```

- Remarks:
> If you pass an empty parameter as delay, it will default to one second (1000 miliseconds).
The minimum is 10 miliseconds. If you use a value lower than 10, it will be considered as 10. The only exception is 0 miliseconds, which are treated as instantly.

---
[Back to overview](index.md)