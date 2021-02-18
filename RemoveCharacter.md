1. Name: RemoveCharacter (Snap)

2. Description: Removes a character from the screen.

3. Parameters

    a. Character Position
    
    The position of the character that is supposed to be removed.

4. Examples:
```json
RemoveCharacter:["Center"];
Snap:["All"];
```

5. Remarks
>There are 3 character positions: "Right", "Left", and "Center".
>
They can be combined. Valid position combinations are: "RightLeft", "RightCenter", "LeftCenter", and "All".
>
This counts for all instructions that use character positions. When omitted, the default value is Center.