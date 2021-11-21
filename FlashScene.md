[Back to overview](index.md)

---
# FlashScene (Flash)
---
### Description
Flashes the screen white.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Duration|Number|Specifies how long the flash should take in miliseconds.|✓|200|

### Examples:
#### Example #1: Flashes the screen for a total of 500ms.
```
1:  Flash:[500];
```

### Remarks:
The duration determines the total time for the flash. This means that both fading in and out each take half the specified time of `Duration`.
Example: `Duration` is set to 200ms. It will then take 100ms to fade the scene to white and then another 100ms to fade out the flash again.

---
[Back to overview](index.md)