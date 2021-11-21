[Back to overview](index.md)

---
# FadeInCharacter (FinChar)
---
### Description
Fades in a character.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Delay|Number|The amount of miliseconds it takes to fade in the character.|✓|1000|
|Position|String|The name of the position used in [LoadCharacter](LoadCharacter.md).|✗|"Center"|

### Examples:
#### Example #1: Fade in the character of the 'Center' position over the span of 3 seconds.
```
1:  FadeInCharacter:[3000];
```

#### Example #2: Fade in the character of the 'Center' position over the span of 1 second.
```
2:  FinChar:[-];
```

#### Example #3: Fade in the character of the 'Left' position over the span of 1.5 seconds.
```
3:  FadeInCharacter:[1500|"Left"];
```

#### Example #4: Fade in the character of the 'Right' position over the span of 1 second.
```
4:  FinChar:[-|"Right"];
```

### Remarks:
If you pass an empty parameter as `Duration`, it will default to one second (1000 miliseconds).  
The minimum is 10 miliseconds. If you use a value lower than 10, it will be considered as 10. The only exception is 0 miliseconds, which are treated as instantly.

---
[Back to overview](index.md)