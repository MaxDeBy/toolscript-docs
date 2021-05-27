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
```

- Remarks:
> None

---
[Back to overview](index.md)