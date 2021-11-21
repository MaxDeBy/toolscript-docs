[Back to overview](index.md)

---
# FadeOutScene  (FoutScene)
---
### Description
Fades out the screen (meaning, character, foreground AND background).

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Duration|Number|The amount of miliseconds it takes to fade out the scene.|✓|1000|
|Color|String|The color (in hex format) the screen should fade to.|✗|"#000000"|

### Examples:
#### Example #1: Fading out the scene over the span of 2.5 seconds.
```
1:  FadeOutScene:[2500];
```

#### Example #2: Fading out the scene over the span of 1 second.
```
1:  FoutScene:[-];
```

#### Example #3: Fading out the scene over the span of 1 second to #32A852 (a shade of green).
```
1:  FoutScene:[-|"32A852"];
```

### Remarks:
If you pass an empty parameter as `Duration`, it will default to one second (1000 miliseconds).  
The minimum is 10 miliseconds. If you use a value lower than 10, it will be considered as 10. The only exception is 0 miliseconds, which are treated as instantly.

---
[Back to overview](index.md)