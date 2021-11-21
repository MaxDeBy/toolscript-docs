[Back to overview](index.md)

---
# PlayFrame
---
### Description
Plays one or more frames.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Frame ID(s)|String|You can pass the IDs of the frames you want to play here. You can pass each frame ID sequentially to play these specific frames in order.|✓|-|

### Examples:
#### Example #1: Play the frame 'TakeThatShout'.
```
1: PlayFrame:["TakeThatShout"];
```

#### Example #2: Play the frames '1', '3', 'TrucyMagic' and '9'.
```
1: PlayFrame:[1|3|"TrucyMagic"|9]; 
```

### Remarks:
If you call a frame with an invalid or non-existant ID, the game will raise an error and crash, rather than ignoring the line.  
See [Frames](Frame.md) for more information about Frames.

---
[Back to overview](index.md)