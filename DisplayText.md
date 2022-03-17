[Back to overview](index.md)

---
# DisplayText (DT)
---
### Description
Displays a dialogue box and a text inside it, displayed letter by letter (by default).

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Character name|String|The text that indicates the speaker. Passing a null character (-) causes the name box to remain hidden.|✓|-|
|Speech|String|The actual dialogue.|✓|-|
|Do not talk|Boolean|If set to true, the character will not switch to the talking animation.|✗|false|
|Is Typewriter|Boolean|If set to true, a typewriter sound blip will be used and the text speed decreases.|✗|false|
|Keep|Boolean|If set to true, the text already existing in the dialogue box will not be erased.|✗|false|
|Silent|Boolean|If set to true, no blips will be played. Useful if voice acting is used.|✗|false|
|Position|String|The name of the position used in [LoadCharacter](LoadCharacter.md).|✗|"Center"|

### Examples:
#### Example #1: Trucy expresses the awkwardness of the situation.
```
1:  DisplayText:["Trucy"|"Well...this is awkward."|false|false|false|false];
```

#### Example #2: A nameless dialogue box to, perhaps, display an objective fact. The character on screen, if any, is not talking.
```
1:  DisplayText:[-|"#GreenSpelling is not my strong suite."|true];
```

#### Example #3: Apollo reacts to his bracelet, with a small pause after 'What?'.
```
1:  DT:["Apollo"|"#Blue(What?#[130]#Blue My bracelet is reacting.)"|true];
```

> The color code `#Blue` has to be repeated after the waiting. Each text code splits a text into a new segment and each segment is automatically set to a white font.

### Remarks:
**You cannot use the pipe (\|) or double quotes (") character in your speech.**

There are multiple ways to specify a blip for a character. Here's how AACT determines what blip should actually be played:
1. If `Silent` is true, no blip will play at all.
2. If `Is Typewriter` is true, the typewriter blip will be used.
3. If `Do not talk` is set to true, the name of the character in the name box will be considered.
4. If the namebox is empty, the character doesn't exist, or `Do not talk` is set to false, the `Position` parameter determines the character that is actually speaking.
5.  If multiple characters are speaking, the blip will be set to the default female if all characters are female. Otherwise it will be set to male.
6. If only a single character is selected (if on the screen or not), and it has a custom blip for the current emote, that custom blip will be used.
7. If there is no custom blip for the current emote, the custom blip of the character itself will be used.
8. If no custom blip exists, the character's gender will determine whether the default male blip or the default female blip will be used.

There are 9 text codes you can use inside a speech:  
- **#Green:** Following text will be displayed green.  
- **#Red:** Following text will be displayed red.  
- **#Blue:** Following text will be displayed blue.  
- **#White:** Following text will be displayed in white.  
- **#Yellow:** Following text will be displayed in yellow.  
- **#Purple:** Following text will be displayed in purple.  
- **#[TIME]:** Replace TIME with a number (no decimal places). The engine will wait that amount in miliseconds before continuing.  
- **#{SPEED}:** Sets the speed mode of the text. The value determines directly how long the delay between blips will be in miliseconds.  
- **#(VARIABLE):** Inserts the value of the specified variable at this position. If the variable doesn't exist, the text "Undefined" will be printed.
- **#\<SPACES\>:** Inserts the specified amount of spaces. A good compensation for the fact there is no way to automatically center text with AACT.

In addition, there are 4 escape codes:
- **\NL:** Inserts a New Line/Line Break
- **\Q:** Inserts double quotes (")
- **\P:** Inserts a pipe (\|)
- **\W:** Can be used to change from **letter** mode, to **word** mode, meaning a message will be then displayed word by word as opposed to letter by letter. This will remain until the next DisplayText with `Keep` set to false.

> The codes are case-sensitive which means if you type them in lowercase they will not work. 

---
[Back to overview](index.md)