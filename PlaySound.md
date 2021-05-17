[Back to overview](index.md)

---
# PlaySound
---
- **Name:** PlaySound (PS)
- **Description:** This instruction plays a sound effect.
- **Parameters:**
  - **Sound name:**  
    The name of the sound effect that should be played.
  - **Delay:**  
    The amount of miliseconds the engine should wait before playing. For example to sync up a deskslam sound with the animation.
  - **Loop (optional):**  
    A boolean value determining if the sound should loop.
 
- Examples:
```
1:  PlaySound:["Deskslam"|600];
2:  PS:["GavelSlam"|300];
3:  PlaySound:["Clap"|0|true];
4:  PS:["Chalkboard"|20|false];
```
 
- Remarks:
> If you don't want the sound to loop, you can omit the 3rd parameter.

---
[Back to overview](index.md)