[Back to overview](index.md)

---
# ButtonChoice (BC)
---
### Description
Displays up to four buttons on the bottom screen and waits until the player has clicked one.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Choice 1|String|The label of the first choice button.|✓|-|
|Choice 2|String|The label of the first choice button.|✗|-|
|Choice 3|String|The label of the first choice button.|✗|-|
|Choice 4|String|The label of the first choice button.|✗|-|
|Frame 1|String|The ID of the Frame for choice 1.|✓|-|
|Frame 2|String|The ID of the Frame for choice 2.|✗|-|
|Frame 3|String|The ID of the Frame for choice 3.|✗|-|
|Frame 4|String|The ID of the Frame for choice 4.|✗|-|

### Examples:
#### Example #1: Giving the player 4 choices, for suggesting a murder weapon.
```
1:  ...
2:  ButtonChoice:["Knife"|"Gun"|"Rope"|"Bat"|1|2|3|4];
3:  ...
```

#### Example #2: Giving the player the choice to accusse the witness or not.
```
1:  ...
2:  BC:["Accuse the witness"|"Don't accuse the witness"|-|-|10|20|-|-];
3:  ...
```

### Remarks:
Each "Choice" parameter must be paired with a "Frame ID" parameter. If `Frame ID 3` is left out, even though `Choice 3` has a value, the third choice will be ignored.

---
[Back to overview](index.md)