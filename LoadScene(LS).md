1. 
Name: LoadScene (LS)


2. 
Description: The LoadScene instruction updates the background AND the character. It also removes a popup if the background changes.


3. 
Parameters:

a. 
Stagename: The name of the background that you want to display. This can be either the actual name you entered in the tool UI or the ID of the background.
                          You can pass an empty argument by using a score "-" (without the quotes) to not change the background. But this will also not remove a popup if one is displayed.


b. 
Character name: The name of the character you want to display. This can be either the actual name you entered in the tool UI or the ID of the character.
                                You can pass an empty argument by using a score "-" to not load a character.


c. 
Emote name: The name of the emote that the character should use. This can be either the actual name you entered in the tool UI or the ID of the emote.
                          You cannot leave this argument empty. It will be ignored however, if you left the charactername empty. So if you did, then you also can use a
                           score for this parameter.


d. 
Play pre: A boolean value indicating whether the preanimation of this emote should be played or not. Use "true" or "false" (without the quotes). True meaning the preanimation will be played.


e. 
Wait for pre: A boolean value indicating whether the engine should wait for the pre animation to wait before continuing with the next line. Use "true" or "false" without the quotes.
                          True meaning that the engine will wait.


f. 
Character position (optional):
     The position of the character.
 


4. 
Example:
```json
LoadScene:["Defense"|"Athena"|"Thinking"|false|false];

LoadScene:[-|"Phoenix"|"Point"|true|true];

LoadScene:["WitnessStand"|-|-|false|false];

LoadScene:["WitnessStand"|-|-|false|false|"Center"];

LoadScene:["JudgeBench"];

LS:["Agency"];
```



5. 
Remarks:
> If you just want to load a scene without loading a character, you can shorten the parameters. In that case you can just use the Stagename parameter as shown as in the
> 
> last example. All the character parameters can be omitted.
> 
> Also notice that it doesn't matter if you type "true" and "false" in capital or in lower case. But it is important you don't use quotes on them.
> 
> Using quotes on string parameters is also not required. It is just for the style. If you put quotes on the beginning or ending of the string, they will be removed.
> 
> If you put them anywhere inside the string, they will be included as a character in that string.
> 
>  
> 
> There are 3 character positions: Right, Left and Center.
> 
> Although, they can be combined. Valid position combinations are: RightLeft, RightCenter, LeftCenter and All.
> 
> This counts for all instructions that use character positions. When omitted, the default value is Center.
