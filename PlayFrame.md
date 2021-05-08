[Back to overview](index.md)

---
# PlayFrame
---
- Name: PlayFrame
- Description: Plays one or more frames.
- Parameters:  
  - **Frame ID(s)**:  
        You can pass the IDs of the frames you want to play here. You can pass each frame ID sequentially to play these specific frames in order.
- Examples:
```
1: PlayFrame:[1|3|"AsshatSucksOnCheeseSticks"|9]; 
2: ->Plays Frame 1, 3, "AsshatSucksOnCheeseSticks" and 9<-
```
- Remarks:
> If you call a frame with an invalid or non-existant ID, the game will raise an error and crash, rather than ignoring the line.  
> See [Frames](Frame.md) for more information about Frames.

---
[Back to overview](index.md)