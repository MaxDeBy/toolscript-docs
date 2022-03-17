[Back to overview](index.md)

---
# LoadCharacter (LC)
---
### Description
Prepares a character spot/position on the screen and sets a character initially.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Position|String|The name of the character position.|✓|"Center"|
|PosX|Number|The placement on the X axis of the current location.|✓|0|
|PosY|Number|The placement on the Y axis of the current location.|✓|0|
|Name|String|The name of the character to load.|✓|-|
|Emote|String|The emote of the character to load.|✗|-|
|PlayPre|Boolean|Whether or not the pre-animation should be played.|✗|\*|
|WaitForPre|Boolean|Whether or not the engine should wait for the pre-animation to finish before continuing.|✗|\*|

### Examples:
#### Example #1: Preparing the 'Center' position at (0, 0) but not loading an initial character.
```
1:  LoadCharacter:[-];
```

#### Example #2: Preparing the 'Right' position at (320, 0) but not loading an initial character.
```
1:  LoadCharacter:["Right"|320];
```

#### Example #3: Preparing the 'Center' position at (0, 0) and loading the character 'Trucy' with the emote 'Bounce'.
```
1:  LoadCharacter:[-|-|-|"Trucy"|"Bounce"];
```

#### Example #3: Preparing the 'Center' position at (0, 0) and loading the character 'Phoenix' with the emote 'Deskslam' but disable the pre animation*.
```
1:  LoadCharacter:[-|-|-|"Phoenix"|"Deskslam"|false|false];
```

### Remarks:
Characters use X and Y positions as well. However, unlike locations, these are not tied to the camera or the logical parent specified in themes. Instead, character positions are tied to the location. If the location moves via [PanCamera](PanCamera.md), so does the character. The coordinates (0, 0) refer to the top left corner.

Setting a character is advisable but not required. Changing the emote or character can be done with the [SetCharacter](SetCharacter.md) Instruction.

*: Not specifying the `PlayPre` and/or `WaitForPre` parameters prompts AACT to use the default values specified in the emote editor of the Asset Maker.

This instruction triggers [HideTextBox](HideTextBox.md).

---
[Back to overview](index.md)