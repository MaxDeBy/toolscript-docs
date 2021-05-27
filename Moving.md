[Back to overview](index.md)

---
# Move
---
- **Name:** Move
- **Description:**  
  Moving describes the action that would correspond to switching locations in the game. The moving instructions are hybrid instructions, meaning their parameters can be values or regular instructions. A moving instruction is construced with the following scheme:
```
1:  Move:{DISPLAY TEXT|INSTRUCTION|HIDDEN};
```
- **Parameters:**
  - **Display Text:**  
    The text that will appear on the button in the moving menu.
  - **Instruction:**  
    The regular instruction that will be executed when clicking on the move button.
  - **Hidden:**  
    The boolean value determining whether or not the moving option is hidden by default.

- Examples:
> None

- Remarks:
> You can define as many move instructions as you like per investigation sequence, however only the first 4 instructions that are not hidden will be shown.

---
[Back to overview](index.md)