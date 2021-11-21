[Back to overview](index.md)

---
# FinishTask
---
### Description
Sets a task to "Done" in a specified tasklist.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|List ID|String|The ID of the tasklist.|✓|-|
|Task ID|Number|The zero-based index of the task.|✓|-|

### Examples:
#### Example #1: Finish the 6th task of the "Gather Evidence" tasklist.
```
1:  FinishTask:["Gather Evidence"|5];
```

### Remarks:
-

---
[Back to overview](index.md)