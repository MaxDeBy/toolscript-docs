[Back to overview](index.md)

---
# PickEvidence
---
- **Name:** PickEvidence (PE)
- **Description:** This instruction forces the user to pick a piece of evidence or profile.
- **Parameters:**
  - **Evidence name:**  
    The name or the ID of the evidence or profile the player has to pick.
  - **Pick Mode:**  
    Determines what the user is actually able to pick. If set to 1, then profiles will be hidden. If set to 2, then evidence will be hidden. Any other value will display both profiles and evidence.
  - **Correct Frame:**  
    The ID of the frame that plays when the player has picked the right evidence.
  - **Wrong Frame:**  
    The ID of the frame that plays when the player has picked the wrong evidence.

- Examples:
```
1:  PickEvidence:["Coffee Mug"|1|3|8];
2:  PE:["Florent"|2|3|9];
3:  PickEvidence:[1];
4:  PE:[2];
```

- Remarks:
> You can omit all but the 2nd parameter (as shown in example 3 and 4). If you do this, the player will be forced to pick a piece of evidence or a profile, like normal, but no frames will be executed. Instead, the result of the player's selection will be stored within 3 variables:
> **Sys_SelectedRecord**: The reference name of the selected record.
> **Sys_SelectedRecordDisplay**: The display name of the selected record.
> **Sys_SelectedRecordIsEvidence**: Will be ```true``` if the selected record is evidence, ```false``` if it is a profile.

---
[Back to overview](index.md)