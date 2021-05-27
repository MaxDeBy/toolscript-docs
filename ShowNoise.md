[Back to overview](index.md)

---
# ShowNoise
---
- **Name:** ShowNoise (Noise)
- **Description:** Displays a noise animation for Mood Matrix.
- **Parameters:**
  - **Start amount:**
    The number the counter should start at.
- **End amount:**  
    The number the counter should end at.

- Examples:
```
1:  ShowNoise:[10|80];
2:  Noise:[20|0];
```

- Remarks
> Depending on whether the start count is higher or lower than the end count, a different animation is played.
>
Also, if the end count is 0 then an ending animation will be played. This occurs only if the start is higher than 0.
>
The noise animation is not tied to a Mood Matrix sequence. It can be displayed at any time and has no impact on anything else.
It is a visual feature, not a functional one. 

---
[Back to overview](index.md)