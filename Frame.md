1. Name: Frame
2. Description: See Remarks
3. Parameters:
    
    a. Frame ID
    
    
    The ID used for calling the Frame with other commands. Can be an integer or a string.
4. Examples:
```json
Frame:[0]<
PlaySound:["GavelSlam"|400];
LoadScene:["Blackout"|"Judge"|"GavelZoom"|true|true|false];
PlayMusic:["Trial"];
LoadScene:["Judge"|"Judge"|"Normal"|false|false|false];
DisplayText:["Judge"|"Court is now in session for the trial of Larry Butz."|false|false|false|false];
>;
Frame:["It's the Butz."]<
LoadScene:["Defense"|"Phoenix"|"Nod"|true|true|false];
DisplayText:["Phoenix"|"The defense is ready, Your Honor."|false|false|false|false];
>;
Frame:[3]<
LoadScene:["Prosecution"|"Miles"|"Bow"|true|true|false];
DisplayText:["Edgrworth"|"The prosecution is ready, as well."|false|false|false|false];
>;
Frame:["It's the Butz"|3];
```
5. Remarks:
> Now, the regular instructions are all fine and dandy, and technically you could just use them; however, you might want to use frames, especially since they are required for some instructions.
> 
> Now what IS a frame? A frame is a container containing one or more regular instructions. It is needed for certain instructions, that require a frame ID (Like the PickEvidence) or that allow the use of a regular instruction (like a hybrid instruction in the investigation). You use a frame when you want to execute multiple instructions within a single instruction. Frames are either invoked automatically by regular instructions that require a frame ID or by executing the "PlayFrame" instruction.
>  
> And now the most important part: How to declare a frame.
> 
> The syntax is relatively easy to understand:
> Frame:[ID]<
> Instructions
> >;
> 
> Important: If you call a frame via the PlayFrame instruction with an invalid or non-existant ID, the game will raise an error and crash, rather than ignoring the line.