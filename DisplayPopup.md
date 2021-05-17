[Back to overview](index.md)

---
# DisplayPopup
---
- **Name:** DisplayPopup (DP)
- **Description:** This instruction displays a popup image.
- **Parameters:**
  - **Popup name:**  
    The name of the popup that should be displayed.
  - **Looping (optional):**  
    A boolean value determining if the popup should loop or not.
 
- Examples:
```
1:  DisplayPopup:["HoldIt"];
2:  DP:["Objection"];
3:  DisplayPopup:["Testimony"|true];
4:  DP:["TakeThat"|false];
```

- Remarks:
>
The popup will not vanish until the background changed.  
If you don't want the popup to loop, you can omit the last parameter.

---
[Back to overview](index.md)