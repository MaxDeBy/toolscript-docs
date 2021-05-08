The Mood Matrix (or short MM) is a gameplay mechanic introduced in Ace Attorney Dual Destinies. It allows the user to visualize a person's true emotions.

The goal is to point out contradicting emotions when compared with the person's spoken testimony. For example, if a witness claims he was angry about something, but the Mood Matrix shows that the witness feels happiness, you can dedude something is wrong.

Example:
```json
MoodMatrix:["AngryMaya"]<
S1:{PlayFrame:[0]|"Happy"|PlayFrame:["ThisFrame"]}
S2:{PlayFrame:[0]}
SCO:<PlayFrame:["ThatFrame"];>
SMF:<PlayFrame:[0];>
>;
```

SCO and SMF are the same as SCO and SEV in the cross examination. The only difference is that in a cross examination, SEV is played when a wrong piece of evidence was presented. 

In the Mood Matrix sequence, the SMF is played when the wrong emotion was pinpointed.

SX is the same idea as in Cross Examinations too, but they work a bit differently here.
In the Mood Matrix syntax, the statement instructions are hybrid instructions, not container instructions. This means that they allow regular instructions, as well as values. Despite this, of course, they still have a set order.
The first parameter is the instruction that is played as the statement. You will probably want to play a frame here that makes the character talk, as well as stops or starts an emoji pulsating.
The second and third parameter are optional.
The second parameter determines a contradicting emotion. If the player pinpoints this emotion, the third parameter is executed.
Afterwards, just like a successful "presenting" ends a Cross Examination, a successful poinpointing ends a Mood Matrix sequence.