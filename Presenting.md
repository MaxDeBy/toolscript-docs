[Back to overview](index.md)

---
# Presenting
---

### Description:
Presenting refers to the action of showing a person a piece of evidence outside of court in order to elicit dialogue or progress the story. There are 4 different types ofpresenting: Evidence, Profile, DefaultEvidence and DefaultProfile. For each piece of evidence you want to be display you use Evidence, and for each profile you wish to display youuse Profile. All other pieces of evidence or profiles are covered through the DefaultEvidence or DefaultProfile, which will be executed when a piece or profile is shown that isn'tcovered throughan Evidence or Profile instruction (for irrelevant evidence and profiles).
A presenting instruction is built like the following scheme:
```
1:  TYPE:{NAME|FIRST PRESENT|SECOND PRESENT};
```

### Parameters

|Name|Type|Description|
|:---:|:---:|:---:|:---:|:---:|
|TYPE|Record|Can be either "Evidence" or "Profile".|
|NAME|String|The name of the evidence or the profile that can be presented.|
|FIRST PRESENT|Regular Instruction|Executed the first time this record is presented.|
|SECOND PRESENT|Regular Instruction|Every subsequent time this record is presented.|

### Examples:
#### Example #1: Present the evidence "Attorney's Badge". The first time it was presented, frame '12' will be executed. Subsequent presentations will execute frame '13'.
```
1:  Evidence:{"Attorney's Badge"|PlayFrame:[12]|PlayFrame:[13]};
```

#### Example #2: Present the profile 'Blue Badger'. The first time it was presented, frame '14' will be executed. Subsequent presentations will execute frame '15'.
```
1:  Profile:{"Blue Badger"|PlayFrame:[14]|PlayFrame:[15]};
```

### Remarks
TYPE can also be "DefaultEvidence" or "DefaultProfile"; however, in that case the hybrid has only one parameter: a regular instruction that gets executed when a piece of evidence or a profile is presented that is not covered by another present instruction. You can define as many DefaultEvidence or DefaultProfile instructions as you want but only the first one of each will be used.
Example: 

```
1:  DefaultEvidence:{PlayFrame:[16]};
2:  DefaultProfile:{PlayFrame:[17]};
```

---
[Back to overview](index.md)