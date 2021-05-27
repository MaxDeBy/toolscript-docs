[Back to overview](index.md)

---
# Mood Matrix
---
The Mood Matrix (or short MM) is a gameplay mechanic introduced in Ace Attorney Dual Destinies&reg;. It allows the user to visualize a person's true emotions.

The goal is to point out contradicting emotions when compared with the person's spoken testimony. For example, if a witness claims he was angry about something, but the Mood Matrix shows that the witness feels happiness, you can dedude something is wrong.

In AACT, a Mood Matrix works almost the same as a [Cross Examination](CrossExamC.md) safe for some minor differences.

Example:
```
1:  MoodMatrix:["AngryMaya"]<
2:  S1:{PlayFrame:[0]|"Happy"|PlayFrame:["ThisFrame"]}
3:  S2:{PlayFrame:[0]}
4:  SCO:<PlayFrame:["ThatFrame"];>
5:  SMF:<PlayFrame:[0];>
6:  >;
```

Unlike a [CrossExamination](CrossExamC.md), a MoodMatrix does not have a MODE.

## Statements
SX is the same idea as in Cross Examinations too, but they work a bit differently here.
In the Mood Matrix syntax, the Statement Instructions are Hybrid Instructions, not Container Instructions. This means that they allow Regular Instructions, as well as values. Despite this, of course, they still have a set order.
The first parameter is the Instruction that is played as the statement. You will probably want to play a frame here that makes the character talk, as well as stops or starts an emoji pulsating.
The second and third parameter are optional.
The second parameter determines a contradicting emotion. If the player pinpoints this emotion, the third parameter is executed.
Afterwards, just like a successful "presenting" ends a Cross Examination, a successful poinpointing ends a Mood Matrix sequence.

## Special Statements
SCO and SMF are the same as SCO and SEV in the cross examination. The only difference is that in a cross examination, SEV is played when a wrong piece of evidence was presented, where as in the Mood Matrix sequence, the SMF is played when the wrong emotion was pinpointed.

---
[Back to overview](index.md)