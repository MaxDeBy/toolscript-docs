[Back to overview](index.md)

---
# Examining
---
Examining is the most complex part of an investigation sequence. An examining container features 4 different hybrid instructions: AllExamined, AlreadyExamined, PointDefault and Point.

## AllExamined
This hybrid instruction contains one parameter which is a regular instruction. It will be executed once the player has examined all spots, defined by a Point instruction.

Example:
```
1:  AllExamined:{PlayFrame:[1]};
```

## AlreadyExamined
This hybrid instruction contains one parameter which is a regular instruction. It will be executed when the player clicks on the "Examine" button after all spots, defined by a Point instruction, have already been examined.

Example:
```
1:  AlreadyExamined:{PlayFrame:[2]};
``` 

## PointDefault
This hybrid instruction contains one parameter which is a regular instruction. It will be executed when the player examines a spot on the upper screen that is not defined by a Point Instruction.

Example:
```
1:  PointDefault:{PlayFrame:[3]};
``` 

## Point
This is the main part of an examination. A point is a spot on the upper screen the player has to click on to invoke some action. The Point instruction is built using the following scheme:
```
Point:{X|Y|OFFSET|FIRST DISCOVER|SECOND DISCOVER};
```

### Parameters

|Name|Type|Description|
|:---:|:---:|:---:|:---:|:---:|
|X|Number|The position on the x-axis.|
|Y|Number|The position on the y-axis.|
|OFFSET|Number|The amount of pixels the cursor is allowed to be off from the defined position.|
|FIRST DISCOVER|Regular Instruction|Gets executed the first time this point was discovered.|
|SECOND DISCOVER|Regular Instruction|Gets executed every subsequent time this point was clicked on.|

Example:
```
1:  Point:{24|48|10|PlayFrame:["DiscoverKnife"]|PlayFrame:["RediscoverKnife]};
``` 

There can be as many Point Instructions as you want.

---
[Back to overview](index.md)