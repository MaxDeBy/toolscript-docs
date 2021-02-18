1. Name: ShowNoise (Noise)

2. Description: Displays a noise animation for Mood Matrix.

3. Parameters

    a. Start amount
    
    The number the counter should start at.
    
    b. End amount
    
    The number the counter should end at.
4. Examples:
```json
ShowNoise:[10|80];
Noise:[20|0];
```

5. Remarks
>Depending on whether the start count is higher or lower than the end count, a different animation is played.
>
Also, if the end count is 0 then an ending animation will be played. This occurs only if the start is higher than 0.
>
The noise animation is not tied to a Mood Matrix sequence. It can be displayed at any time and has no impact on anything else.
It is a visual feature, not a functional one. 