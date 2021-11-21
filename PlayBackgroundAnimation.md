[Back to overview](index.md)

---
# PlayBackgroundAnimation (PlayBackAnim)
---
### Description
Starts the currently prepared animated background. Does nothing if no animation was prepared.

### Parameters
This instruction has no parameters.

### Examples:
#### Example #1: Playing the prepared background animation, if it exists.
```
1:  PlayBackgroundAnimation;
```

### Remarks:
For this Instruction to work, you need to execute [PrepareBackgroundAnimation](PrepareBackgroundAnimation.md) first.  

If called while the animation has not been fully loaded yet, the game won't freeze but this instruction will suspend it's execution asynchronously until the animation is ready to be rendered. 
So make sure, to call [PrepareBackgroundAnimation](PrepareBackgroundAnimation.md) early enough.

---
[Back to overview](index.md)