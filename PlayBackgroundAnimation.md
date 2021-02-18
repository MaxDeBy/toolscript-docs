1. Name: PlayBackgroundAnimation (PlayBackAnim)

2. Description: Plays an animation in the background.

3. Parameters

    a. Animation filename

    The filename of the GIF animation, without the file ending.

    b. Loop

    A boolean value representing whether or not the animation should loop.

4. Examples:
```json
PlayBackgroundAnimation:["CaseIntro"|false];
PlayBackgroundAnimation:["Perceive"|true];
```

5. Remarks
>The file for the specified animation has to be within the "Misc" folder which can be found under Assets>Images>Misc.
>
The file must be a GIF animated file.