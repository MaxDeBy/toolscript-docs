[Back to overview](index.md)

---
# MakeTaskList
---
### Description
Creates a list with a specified amount of tasks.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|ID|String|The ID of the tasklist.|✓|-|
|Amount|Number|The amount of tasks in the list.|✓|1|
|Completion Frame|String|The ID of the frame to be executed upon completion of all tasks.|✓|"SomeFrame"|

### Examples:
#### Example #1: Create a list 'InvestigateOffice' with 5 tasks. When all tasks are completed, the Frame '3' should be executed.
```
1:  MakeTaskList:["InvestigateOffice"|5|3];
```

### Remarks:
Task lists only exist within a chapter. If you create a list during chapter A, it will not be available in chapter B.

---
[Back to overview](index.md)