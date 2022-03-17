[Back to overview](index.md)

---
# HideTextBox  (HTB)
---
### Description
Hides the textbox, with a fade animation or without.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Fade|Boolean|Whether the textbox should disappear by fading or instantly.|✗|true|

### Examples:
#### Example #1: Hiding the textbox with a fading animation.
```
1:  HideTextBox:[true];
or
2:  HideTextBox:[-];
```

#### Example #2: Hiding the textbox instantly.
```
1:  HTB:[false];
```

### Remarks:
This instruction breaks a syntax rule: Using a null character is not necessary. `HTB;` and `HideTextBox;` are valid and will be interpreted as `HTB:[true];` and `HideTextBox:[true];` respectively.

[SetCharacter](SetCharacter.md) will execute this instruction as well unless the `WaitForPre` parameter is `false` and there is a [DisplayText](DisplayText.md) instruction following immediately afterwards.
If these conditions are not met, [SetCharacter](SetCharacter.md) will execute this instruction as `HideTextBox:[true];`.

[LoadCharacter](LoadCharacter.md) will execute this instruction as well unless the `WaitForPre` parameter is `false` and there is a [DisplayText](DisplayText.md) instruction following immediately afterwards.
If these conditions are not met, [LoadCharacter](SetCharacter.md) will execute this instruction as `HideTextBox:[false];`.

---
[Back to overview](index.md)