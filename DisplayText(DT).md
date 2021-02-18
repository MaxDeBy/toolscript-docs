1. 
Name: DisplayText (DT)


2. 
Description: This instruction displays the actual text in a textbox. It also has a lot of parameters to change its behaviour.


3. 
Parameters:


a. 
Character name:
The text that should be written in the name box. Like the character's name or something like "???". If you pass an empty argument (by using a "-", without the quotation marks), the namebox will not be displayed.


b. 
Speech:
The actual text that should be displayed. 


c. 
Do not talk:
 A boolean value that indicates whether the character should move their mouth while talking or not. True meaning the mouth will **not** move.


d. 
Is typewriter:
A boolean value that indicates whether a typewriter sound should be played, rather than the character blips. True meaning the typewriter sound will be moved.


e. 
Keep:
A boolean value that indicates whether the text from the last textbox should be included in this textbox. For example if you want to change the emote during a speech.


f. 
Silent:
A boolean value that indicates whether no blips should be played during this speech. True meaning there will be no sounds. This has higher priority than the "Is typewriter" parameter.


g. 
Character position (optional):
The position of the character that is supposed to talk.
 


4. 
Examples:
```json
DisplayText:["Trucy"|"Well...this is awkward."|false|false|false|false];

DisplayText:[-|"--- What I saw ---"|true|false|false|true];

DisplayText:[-|"#GreenDoom is to lazy for a third example."|true|true|false|false];

DisplayText:[-|"#GreenDoom also cannot spell properly."|true|true|false|false|"Right"];

DT:["Apollo"|"#Blue(What?#[130] My bracelet is reacting.)"|true|false|false|false];
```

 



5. 
Remarks:
> The charactername does not influence what character will actually speak. Obviously it will always be the character that's currently on the screen. The charactername is ONYL for the namebox.
> 
> You cannot use certain characters in the speech. This includes pipes ("|"), square brackets "[ ]" and the arrows (used for instruction brackets) "< >".
> 
>  
> 
> Also there are 8 codes you can use inside a speech:
> 
> 
> 
> • #Green: Following text will be displayed green.
> 
> 
> • #Red: Following text will be displayed red.
> 
> 
> • #Blue: Following text will be displayed blue.
> 
> 
> • #White: Following text will be displayed in white.
> 
> 
> • #Yellow: Following text will be displayed in yellow.
> 
> 
> • #Purple: Following text will be displayed in purple.
>
>
> • The textcode #Q, when used, will be replaced with a quote (").
>
>
> • The textcode #P, when used, will be replaced with a pipe (|).
> 
> 
> • #[TIME]: Replace TIME with a number (no decimal places). The engine will wait that amount in miliseconds before continuing.
> 
> 
> • #{SPEED}: Sets the speed mode of the text. The value determines directly how long the delay between blips will be >in miliseconds.
> 
> • The textcode \W can be used to change from 'letter' mode, to 'word' mode, meaning a message will be then displayed word by word as opposed to letter by letter.
>
>
> • #(VARIABLE): Inserts the value of the specified variable at this position. If the variable doesn't exist, an empty string will be inserted.
> 
> 
> • \NL: New Line.
> 
>  
> 
> The codes are case-sensitive which means if you type them in lowercase they will not work.
> 
>  
> 
> The font in the textbox is not mono-sized. Meaning a "W" will take more space than an "L".
> 
> The textbox consists of three rows which hold space for 21 Ws per row. So the whole textbox has space for 63 Ws. And yes, it automatically breaks the line.
> 
>  
> 
> There are 3 character positions: Right, Left and Center.
> 
> Although, they can be combined. Valid position combinations are: RightLeft, RightCenter, LeftCenter and All.
> 
> This counts for all instructions that use character positions. When omitted, the default value is Center.