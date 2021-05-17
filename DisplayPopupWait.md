[Back to overview](index.md)

---
# DisplayPopupWait
---
- **Name:** DisplayPopupWait (DPW)
- **Description:** This instruction displays a popup image and waits until the animation has finished playing.
- **Parameters:**
  - **Popup name:**  
    The name of the popup that should be displayed.
 
- Examples:
```
1:  DisplayPopupWait:["HoldIt"];
2:  DPW:["Testimony"];
```

- Remarks:
>
The popup will not vanish until the background changed.  
This Instruction does not support looping, for obvious reasons. If you need a looping popup, use [DisplayPopup](DisplayPopup.md) instead.

---
[Back to overview](index.md)