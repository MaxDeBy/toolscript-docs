[Back to overview](index.md)

---
# HideHealth
---
- **Name:** HideHealth (HH)
- **Description:** This instruction hides the health bar in the top right corner.
- **Parameters:**
  - **Slide Animation**:  
    A boolean value that determines whether or not the health bar should vanish with a slide animation.

- Examples:
```
1:  HideHealth:[true];
2:  HH:[false];
```

- Remarks:
>
There are two health bars. The first is the regular health bar that is usually displayed during a trial and a second one for the psyche locks. The health bar is on the left side, as opposed to the psyche bar which is on the right side. There is also a special frame ID `GameOver` which you can give to a frame to mark it as a GameOver frame. A GameOver frame will be called if the health drops down to 0. Once the content of the GameOver frame has been executed, the game will automatically end.

---
[Back to overview](index.md)