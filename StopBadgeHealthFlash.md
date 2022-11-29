[Back to overview](index.md)

---
# StopBadgeHealthFlash (StopBH)
---
### Description
Stops all badges of the badge healthbar from flashing.

### Parameters
This instruction has no parameters.

### Examples:
#### Example #1: Just stop.
```
1: ...
2: StopBadgeHealthFlash;
3: ...
```

### Remarks:
The badge healthbar is independant from the regular healthbar and they can both be used in the same game without influencing each other. However, the badge healthbar is still a healthbar. This means, that if the last badge is [destroyed](DestroyBadges.md),
the frame with the ID `GameOver` will be executed, if it exists.

The appearance and position of the healthbar can be modified via themes.

---
[Back to overview](index.md)