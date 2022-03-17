[Back to overview](index.md)

---
# SetTimer (Tmr)
---
### Description
Starts a timer and optionally executes a frame after the specified amount of time.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Time|Number|The amount of miliseconds the timer should go.|✓|60000|
|TextFormat|String|The format of the text that can be displayed with the timer.|✓|"SS"|
|Frame ID|String|This frame, if it exists, will be executed once the timer runs out.|✗|-|

### Examples:
#### Example #1: Set a timer for 20 seconds and do nothing after. The timer will have the format "SS".
```
1:  SetTimer:[20000|"SS"];
```

#### Example #2: Set a timer for 4 minutes and execute a frame afterwards. The timer will have the format "mm:ss,fff".
```
1:  Tmr:[240000|"mm:ss,fff"|"TimerEnd"];
```

### Remarks:
> Be absolute sure of what you're doing if you use the Frame ID parameter. This frame may be executed at any time once the timer runs out and may interrupt other stuff currently happening. It's not recommended to display dialog or anything similar in that frame. Again: **BE ABSOLUTE SURE OF WHAT YOU'RE DOING!**

The format parameter can be any text, but certain codes are replaced with some numbers:

|Code|Replaced with|
|:---|:---|
|HH|Total hours preceded by a 0, if less than 10.|
|H|Total hours.|
|MM|Total minutes preceded by a 0, if less than 10.|
|M|Total minutes.|
|SS|Total seconds preceded by a 0, if less than 10.|
|S|Total seconds.|
|FFF|Total miliseconds preceded by two 0s, if less than 10 or one 0 if less than 100.|
|FF|Total miliseconds preceded by a 0, if less than 10.|
|F|Total miliseconds.|
|hh|Hours preceded by a 0, if less than 10.|
|h|Hours.|
|mm|Minutes preceded by a 0, if less than 10.|
|m|Minutes.|
|ss|Seconds preceded by a 0, if less than 10.|
|s|Seconds.|
|fff|Miliseconds preceded by two 0s, if less than 10 or one 0 if less than 100.|
|ff|Miliseconds preceded by a 0, if less than 10.|
|f|Miliseconds.|

> AACT's text render abilities are very primitive at the moment. As such, there is currently no way to display a good looking timer text. A "DisplayTimer" instruction (which would display a text showing a countdown of the timer) will be added in a future version, after the text render abilities have been enhanced.

---
[Back to overview](index.md)