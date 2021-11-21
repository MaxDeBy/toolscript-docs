[Back to overview](index.md)

---
# FadeInScene  (FinScene)
---
### Description
Fades the screen (meaning, character, foreground AND background) back in.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Duration|Number|The amount of miliseconds it takes to fade in the scene.|✓|1000|

### Examples:
#### Example #1: Fading in the scene over the span of 2.5 seconds.
```
1:  FadeInScene:[2500];
```

#### Example #2: Fading in the scene over the span of 1 second.
```
1:  FinScene:[-];
```

### Remarks:
If you pass an empty parameter as `Duration`, it will default to one second (1000 miliseconds).  
The minimum is 10 miliseconds. If you use a value lower than 10, it will be considered as 10. The only exception is 0 miliseconds, which are treated as instantly.

---
[Back to overview](index.md)