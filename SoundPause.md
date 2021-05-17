[Back to overview](index.md)

---
# SoundPause
---
- **Name:** SoundPause
- **Description:** A second way of pausing for a little. Instead of using miliseconds, you can input the name of a sound effect, and the engine will wait until the sound effect's full duration has passed before it proceeds.
- **Parameters:**
  - **Sound name:**  
    The name of the soundeffect which length should be waited for.

- Examples:
```
1:  SoundPause:["Deskslam"];
```

- Remarks:
> 
The engine will wait, regardless if the sound is actually played or not.  
Note that this can cause crashes if the sound file is not encoded properly. This is not a reliable way to wait for something to finish.  
Only use this Instruction if there is nothing visually to wait for. If you only need to wait for an animation to finish, use [DisplayPopupWait](DisplayPopupWait.md) or the `Wait for pre` parameter in the [LoadScene](LoadScene.md) Instruction.

---
[Back to overview](index.md)