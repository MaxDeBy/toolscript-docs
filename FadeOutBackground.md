[Back to overview](index.md)

---
# FadeOutBackground (FoutBg)
---
### Description
Fades out the background of the screen.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Duration|Number|The amount of miliseconds it takes to fade out the background.|✓|1000|

### Examples:
#### Example #1: Slowly fade out the background over the span of 5 seconds.
```
1:  FadeOutBackground:[5000];
```

#### Example #2: Fade out the background with the default duration of 1 second.
```
1:  FoutBg:[-];
```

### Remarks:
If you pass an empty parameter as `Duration`, it will default to one second (1000 miliseconds).  
The minimum is 10 miliseconds. If you use a value lower than 10, it will be considered as 10. The only exception is 0 miliseconds, which are treated as instantly.

---
[Back to overview](index.md)