[Back to overview](index.md)

---
# Pause
---
### Description
Tells the engine to wait a certain amount of time before executing the next line in the script.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Duration|Number|The amount of miliseconds the engine should wait before continuing.|✓|10|

### Examples:
#### Example #1: Wait for one second before continuing.
```
1:  Pause:[1000];
```

### Remarks:
Due to technical reasons, a delay shorter than 10ms is not possible. Everything below 10 (including 0) will be interpreted as 10.

---
[Back to overview](index.md)