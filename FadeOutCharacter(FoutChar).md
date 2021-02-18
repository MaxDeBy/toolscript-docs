
1. 
Name: FadeOutCharacter (FoutChar)


2. 
Description: Fades out the character of the screen.


3. 
Parameters:


a. 
Delay
     The amount of miliseconds it takes to fade out the character.


b. 
Character position (optional)
     The position of the character that is supposed to fade out
 


4. 
Examples:
```json
FadeOutCharacter:[1000];

FoutChar:[-];

FadeOutCharacter:[1000|"RightLeft"];

FoutChar:[-|"RightLeft"];
```

 



5. 
Remarks:

> If you pass an empty parameter as delay, it will default to one second (1000 miliseconds).
> 
>  
> 
> There are 3 character positions: Right, Left and Center.
> 
> Although, they can be combined. Valid position combinations are: RightLeft, RightCenter, LeftCenter and All.
> 
> This counts for all instructions that use character positions. When omitted, the default value is Center.