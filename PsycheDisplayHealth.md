1. Name: PsycheDisplayHealth (PsyDH)

2. Description: Displays the psyche bar.

3. Parameters:

    a. Slide animation

    A boolean value that determines whether the psyche bar should appear with a slide animation.
4. Examples:
```json
PsycheDisplayHealth:[true];
PsyDH:[false];
```

5. Remarks:
>
 Starting from 1.4, there are two health bars. The first is the regular health bar that is usually displayed during a trial and a second one for the psyche locks. The second bar is refered to as "psyche bar" in AACT. The psyche bar is on the left side, as opposed to the normal health bar which is on the right side. It supports the same features as the regular health bar. There is also a special frame container, called PsycheOver, which is just like the GameOver frame. While the GameOver frame automatically ends the game, the PsycheOver frame does not, so it can be used multiple times.