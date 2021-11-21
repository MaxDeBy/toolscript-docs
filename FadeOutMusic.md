[Back to overview](index.md)

---
# FadeOutMusic (FoutM)
---
### Description
Fades out the currently playing music.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Duration|Number|The amount of miliseconds it takes to fade out the music.|✓|1000|

### Examples:
#### Example #1: Fading out the foreground over the span of 3 seconds.
```
1:  FadeOutMusic:[3000];
```

#### Example #2: Fading out the foreground over the span of 1 second.
```
1:  FoutM:[-];
```

### Remarks:
If you pass an empty parameter as `Duration`, it will default to one second (1000 miliseconds).  
The minimum is 10 miliseconds. If you use a value lower than 10, it will be considered as 10. The only exception is 0 miliseconds, which are treated as instantly.

---
[Back to overview](index.md)