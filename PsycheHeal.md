1. Name: PsycheHeal (PsyH)

2. Description: Increases the health of the psyche bar.

3. Parameters:
    
    a. Amount
    
    The amount of health to be added.
4. Examples:
```json
PsycheHeal:[20];
PsyH:[50];
```

5. Remarks:
>This instruction will automatically display the psyche bar.
>
 Starting from 1.4, there are two health bars. The first is the regular health bar that is usually displayed during a trial and a second one for the psyche locks. The second bar is refered to as "psyche bar" in AACT. The psyche bar is on the left side, as opposed to the normal health bar which is on the right side. It supports the same features as the regular health bar. There is also a special frame container, called PsycheOver, which is just like the GameOver frame. While the GameOver frame automatically ends the game, the PsycheOver frame does not, so it can be used multiple times.