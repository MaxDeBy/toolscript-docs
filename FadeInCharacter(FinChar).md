1. 
Name: FadeInCharacter (FinChar)


2. 
Description: Fades in the character of the screen.


3. 
Parameters:


a. 
Delay
     The amount of miliseconds it takes to fade in the character.


b. 
Character position (optional)
     The position of the character that is supposed to fade in.
 


4. 
Examples:
```json
FadeInCharacter:[1000];

FadeInCharacter:[1000|"Left"];

FinChar:[-];

FinChar:[-|"Left"];

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