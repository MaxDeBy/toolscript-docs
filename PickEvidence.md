[Back to overview](index.md)

---
# PickEvidence (PE)
---
### Description
This instruction forces the user to pick a piece of evidence or profile.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Name|String|The name or the ID of the evidence or profile the player has to pick.|✗|-|
|Mode|Number|1 = Show Evidence, 2 = Show Profiles, everything else = Show both|✓|0|
|Correct Frame|String|The ID of the frame that plays when the player has picked the right evidence.|✗|-|
|Wrong Frame|String|The ID of the frame that plays when the player has picked the wrong evidence.|✗|-|

### Examples:
#### Example #1: Prompting the player to choose the evidence 'Coffee Mug', while hiding profiles. If the player chooses the mug, frame 'CoffeeChosen' plays. Otherwise, frame '8' plays.
```
1:  PickEvidence:["Coffee Mug"|1|"CoffeeChosen"|8];
```

#### Example #2: Prompting the player to pick the profile 'Florent', while hiding the evidence. If the player chooses Florent, frame 'FlorentChosen' plays. Otherwise, frame '9' plays.
```
1:  PE:["Florent"|2|"FlorentChosen"|9];
```

#### Example #3: Prompting the player to choose any piece of evidence.
```
1:  PickEvidence:[1];
```

#### Example #4: Prompting the player to choose any profile.
```
2:  PE:[2];
```

### Remarks:
You can omit all but the 2nd parameter (as shown in example 3 and 4). If you do this, the player will be forced to pick a piece of evidence or a profile, like normal, but no frames will be executed. Instead, the result of the player's selection will be stored within 3 variables:
- **Sys_SelectedRecord**: The reference name of the selected record.
- **Sys_SelectedRecordDisplay**: The display name of the selected record.
- **Sys_SelectedRecordIsEvidence**: Will be `true` if the selected record is evidence, `false` if it is a profile.

This version can also be used in Cross Examinations. Using the PickEvidence instruction with only one parameter in a Cross Examination will always cause the SEV instruction to be executed, if it exists. If not, the next statement will be executed.

---
[Back to overview](index.md)