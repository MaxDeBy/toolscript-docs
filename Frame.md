[Back to overview](index.md)

---
# Frame
---
Now, the regular instructions are all fine and dandy, and technically you could just use them; however, you might want to use frames, especially since they are required for some instructions.

Now what IS a frame? A frame is a container containing one or more regular instructions. It is needed for certain instructions, that require a frame ID (Like the PickEvidence) or that allow the use of a regular instruction (like a hybrid instruction in the investigation). You use a frame when you want to execute multiple instructions within a single instruction. Frames are either invoked automatically by regular instructions that require a frame ID or by executing the [PlayFrame](PlayFrame.md) instruction.
 
And now the most important part: How to declare a frame.

The syntax is relatively easy to understand:
```
1:  Frame:[ID]<
2:  Instructions
3:  >;
```

Example:
```
1:  Frame:[0]<
2:  PlaySound:["GavelSlam"|400];
3:  LoadScene:["Blackout"|"Judge"|"GavelZoom"|true|true|false];
4:  PlayMusic:["Trial"];
5:  LoadScene:["Judge"|"Judge"|"Normal"|false|false|false];
6:  DisplayText:["Judge"|"Court is now in session for the trial of Larry Butz."|false|false|false|false];
7:  >;
8:  Frame:["It's the Butz."]<
9:  LoadScene:["Defense"|"Phoenix"|"Nod"|true|true|false];
10: DisplayText:["Phoenix"|"The defense is ready, Your Honor."|false|false|false|false];
11: >;
12: Frame:[3]<
13: LoadScene:["Prosecution"|"Miles"|"Bow"|true|true|false];
14: DisplayText:["Edgrworth"|"The prosecution is ready, as well."|false|false|false|false];
15: >;
16: PlayFrame:["It's the Butz"|3];
```

---
[Back to overview](index.md)