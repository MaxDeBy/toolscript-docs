[Back to overview](index.md)

---
# GameOver
---
### Description
Requests the game to end.

### Parameters
This instruction has no parameters.

### Examples:
#### Example #1: Request a game over.
```
1:  GameOver;
```

### Remarks:
If this instruction is called, the game doesn't end immediately. Usually, the engine waits for a dialog to finish first.
For example, if this instruction is called during a press frame of [Cross Examinations](CrossExamC.md), then the game will end **after** the press frame has finished executing.

This instruction will execute the GameOver frame, if it exists.

---
[Back to overview](index.md)