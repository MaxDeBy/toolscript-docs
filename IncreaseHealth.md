[Back to overview](index.md)

---
# IncreaseHealth
---
- **Name:** IncreaseHealth (Heal)
- **Description:** Increases the amount of health.
- **Parameters:**
  - **Amount:**  
    The amount of health to add.

- Examples:
```
1:  IncreaseHealth:[20];
2:  Heal:[50];
```

- Remarks:
> The maximum amount of health is 100. 
The health bar will automatically be displayed when the health is changed, provided it wasn't already displayed
>
> Should the health fall to 0 or below, a the Frame with the ID `GameOver` will be called, should it exist. Afterwards, the game will end.

---
[Back to overview](index.md)