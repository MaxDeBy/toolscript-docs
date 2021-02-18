1. Name: PickEvidence (PE)
2. Description: This instruction forces the user to pick a piece of evidence or profile.
3. Parameters:
   
    a. Evidence name
   
    The name or the ID of the evidence or profile the player has to pick.
    
    b. Pick Mode
    
    Determines what the user is actually able to pick. If set to 1, then profiles will be hidden. If set to 2, then evidence will be hidden. Any other value will display both profiles and evidence.
    
    c. Correct Frame
    
    The ID of the frame that plays when the player has picked the right evidence.
    
    d. Wrong Frame
    
    The ID of the frame that plays when the player has picked the wrong evidence.
4. Examples:
```json
PickEvidence:["Coffee Mug"|1|3|8];
PE:["Florent"|2|3|9];
```
5. Remarks:
> None