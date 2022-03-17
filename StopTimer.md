[Back to overview](index.md)

---
# StopTimer (StpTmr)
---
### Description
Stops the currently running timer, if there is one.

### Parameters
This instruction has no parameters.

### Examples:
#### Example #1: Stop a timer.
```
1:  StopTimer;
```

### Remarks:
If the currently running timer would've executed a frame at the end, it will not be executed if the timer is stopped with this instruction.

> AACT's text render abilities are very primitive at the moment. As such, there is currently no way to display a good looking timer text. A "DisplayTimer" instruction (which would display a text showing a countdown of the timer) will be added in a future version, after the text render abilities have been enhanced.

---
[Back to overview](index.md)