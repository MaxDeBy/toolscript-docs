[Back to overview](index.md)

---
# SetCharacter (SetChar)
---
### Description
Changes the emote and optionally the character of a character position.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Emote|String|The name of the emote to switch to.|✓|-|
|Position|String|The position of the character to set the emote of.|✗|"Center"|
|Character name|String|If set, replaces the character of the position.|✗|*Current name of the position.*|
|PlayPre|Boolean|Whether or not the pre-animation should be played.|✗|\*|
|WaitForPre|Boolean|Whether or not the engine should wait for the pre-animation to finish before continuing.|✗|\*|

### Examples:
#### Example #1: Load the 'Bounce' emote of the character currently in the 'Center' position.
```
1:  SetCharacter:["Bounce"];
```

#### Example #2: Load the 'Deskslam' emote of the character currently in the 'Right' position.
```
1:  SetCharacter:["Deskslam"|"Right"];
```

#### Example #3: Replacing the character of the 'Left' position with the character 'Apollo' and loading the 'Point' emote.
```
1:  SetCharacter:["Point"|"Left"|"Apollo"];
```

#### Example #4: Replacing the character of the 'Center' position with the character 'Apollo' and loading the 'Point' emote, but explicitely specifying the pre animation should not play.*
```
1:  SetCharacter:["Point"|-|"Apollo"|false|false];
```

### Remarks:
If the specified emote doesn't exist for the character, this instruction does nothing.

*: Not specifying the `PlayPre` and/or `WaitForPre` parameters prompts AACT to use the default values specified in the emote editor of the Asset Maker.

This instruction triggers [HideTextBox](HideTextBox.md).

---
[Back to overview](index.md)