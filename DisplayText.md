[Back to overview](index.md)

---
# DisplayText
---
- **Name:** DisplayText (DT)
- **Description:** This instruction displays the actual text in a textbox. It also has a lot of parameters to change its behaviour.
- **Parameters:**
  - **Character name:**  
    The text that should be written in the name box. Like the character's name or something like "???". If you pass an empty argument (by using a "-", without the quotation marks), the namebox will not be displayed.
  - **Speech:**  
    The actual text that should be displayed. 
  - **Do not talk:**  
    A boolean value that indicates whether the character should move their mouth while talking or not. True meaning the mouth will **not** move.
  - **Is typewriter:**  
    A boolean value that indicates whether a typewriter sound should be played, rather than the character blips. True meaning the typewriter sound will be moved.
  - **Keep:**  
    A boolean value that indicates whether the text from the last textbox should be included in this textbox. For example if you want to change the emote during a speech.
  - **Silent:**  
    A boolean value that indicates whether no blips should be played during this speech. True meaning there will be no sounds. This has higher priority than the "Is typewriter" parameter.
  - **Character position (optional):**  
    The position of the character that is supposed to talk.
 
- Examples:
```
1:  DisplayText:["Trucy"|"Well...this is awkward."|false|false|false|false];
2:  DisplayText:[-|"--- What I saw ---"|true|false|false|true];
3:  DisplayText:[-|"#GreenDoom is to lazy for a third example."|true|true|false|false];
4:  DisplayText:[-|"#GreenDoom also cannot spell properly."|true|true|false|false|"Right"];
5:  DT:["Apollo"|"#Blue(What?#[130] My bracelet is reacting.)"|true|false|false|false];
```

- Remarks:
> 
If the `Do not talk` parameter is set to true, the `Character name` parameter is used to determine what blips should be played. This is useful for first-person dialog.  
>
You cannot use the pipe (\|) or double quotes (") character in your speech.  
> 
There are 9 text codes you can use inside a speech:  
> • **#Green:** Following text will be displayed green.  
> • **#Red:** Following text will be displayed red.  
> • **#Blue:** Following text will be displayed blue.  
> • **#White:** Following text will be displayed in white.  
> • **#Yellow:** Following text will be displayed in yellow.  
> • **#Purple:** Following text will be displayed in purple.  
> • **#[TIME]:** Replace TIME with a number (no decimal places). The engine will wait that amount in miliseconds before continuing.  
> • **#{SPEED}:** Sets the speed mode of the text. The value determines directly how long the delay between blips will be in miliseconds.  
> • **#(VARIABLE):** Inserts the value of the specified variable at this position. If the variable doesn't exist, an empty string will be inserted.  
> 
> In addition, there are three escape codes which will be replaced with a certain character:  
> • **\NL:** New Line/Line break  
> • **\Q:** Double quotes (")  
> • **\P:** Pipe (\|)    
> 
> And last but not least the special escape code **\W:**  
> • The textcode \W can be used to change from `letter` mode, to `word` mode, meaning a message will be then displayed word by word as opposed to letter by letter.  
> 
> The codes are case-sensitive which means if you type them in lowercase they will not work.  
> 
> The font in the textbox can be adjusted via themes.  
> 
> There are 3 character positions: `Right`, `Left` and `Center`.  
> Although, they can be combined. Valid position combinations are: `RightLeft`, `RightCenter`, `LeftCenter` and `All`.
> 
> This counts for all instructions that use character positions. When omitted or invalid, the default value is `Center`.

---
[Back to overview](index.md)