1. Name: Move

2. Description: Moving describes the action that would correspond to switching locations in the game. The moving instructions are hybrid instructions, meaning their parameters can be values or regular instructions. A moving instruction is construced with the following scheme:
```
Move:{DISPLAY TEXT|INSTRUCTION|HIDDEN};
```

3. Parameters:

    a. Display Text
    
    The text that will appear on the button in the moving menu.
    
    b. Instruction
    
    The regular instruction that will be executed when clicking on the move button.

    c. Hidden

    The boolean value determining whether or not the moving option is hidden by default.
4. Examples:
> None
5. Remarks:
>You can define as many move instructions as you like per investigation sequence, however due to the limited screen space only the first 4 instructions that are not hidden will be shown.
> 
The moving instructions are inside the Moving container in the investigation.