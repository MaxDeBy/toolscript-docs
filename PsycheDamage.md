[Back to overview](index.md)

---
# PsycheDamage
---
- **Name:** PsycheDamage (PsyD)
- **Description:** Reduces the health of the psyche bar.
- **Parameters:**
  - **Amount:**  
    The amount of health the bar is reduced by.

- Examples:
```
1:  PsycheDamage:[20];
2:  PsyD:[50];
```

- Remarks:
> This instruction will automatically display the psyche bar.
>
There are two health bars. The first is the regular health bar that is usually displayed during a trial and a second one for the psyche locks. The second bar is refered to as "psyche bar" in AACT. The psyche bar is on the right side, as opposed to the normal health bar which is on the left side. It supports the same features as the regular health bar. There is also a special frame ID `PsycheOver` which is just like the `GameOver` frame ID. While the GameOver frame automatically ends the game, the PsycheOver frame does not, so it can be used multiple times.

---
[Back to overview](index.md)