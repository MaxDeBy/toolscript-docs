[Back to overview](index.md)

---
# Cross Examination
---
The Cross Examination Instruction, or for short CE Instruction, is obviously used for processing a Cross Examination. The container itself is defined similar to a frame:

```
1:  CrossExamination:[ID|MODE]<
2:  INSTRUCTIONS
3:  >;
```
**MODE** refers to how the Cross Examination can be finished. If set to 1, the Cross Examination will only end if the player pressed all statements at least once.
Every other number means a contradiction has to be found. If you want to combine it, meaning you want the Cross Examination to end either way, set it to 1. 

That will take care of the press condition. And to end it by objecting, execute the newly added FinishCrossExam Instruction in a frame that gets executed through the PickEvidence Instruction mentioned below.
 
A Cross Examination, just like Frames, is a Container Instructions, meaning they can host multiple Instructions inside. Other than Frames, however, you are limited to what kind of Instructions you can add to the CEs body.

## Statements
In a Cross Examination, you only can use Statement Instructions. Statement Instructions are also Container Instructions, hence they use the Container brackets "<" and ">".
But they are also limited. But rather than the kinds they are limited to, Statement Instructions are limited by number. They only allow two plus one optional Regular Instruction. Any more or any less will fail to load the script. 

A statement Instruction is built like this:

```
1:  SNUM:<Instruction1;Instruction2;Instruction3;>
```

> Statement Instructions do NOT end with a semicolon.
 
**NUM** is the number of the statement Instruction. It always starts with "1". The upper limit is 10. So you can have a maximum of 10 statements per CE.

Now Instruction 1, 2, and 3 can be any Regular Instruction you want. But it only makes sense for two Instructions.

Instruction 1 and 2 should be a [PlayFrame](PlayFrame.md) Instruction. Instruction 1 will be executed when the statement is being played. So it should contain a [PlayFrame](PlayFrame.md) Instruction that plays a Frame with a green text.  
Instruction 2 will be executed while pressing, meaning when the player clicks on the "Press" button.  
Instruction 3 is optional. But if you use it, it **has** to be a [PickEvidence](PickEvidence.md) Instruction. Add this to the statement that contains a contradiction to make it objectionable.

> Attention: Currently there can only be one statement marked as "contradiction". If you add the PickEvidence to multiple statements, only the first one will be considered.

## Special Statements
Then there are two other Statement Instructions. They don't actually have anything to do with a statement, however.
These are called SCO and SEV and each of them only allows a single Regular Instruction, which, again, should be a [PlayFrame](PlayFrame.md) Instruction.
The SCO will be executed after the last statement has been displayed. You should use  it for discussions with the counsel like in the games which usually gives a vague hint on where to look for.
The SEV will be executed when the player objects (pressing "Present") in a statement that doesn't have a contradiction. 

An example Cross Examination could look like this:

```
1:  CrossExamination:[0|1]<
2:     S1:<Frame[1];Frame[5];>   
3:     S2:<Frame[2];Frame[6];PickEvidence:["Autopsy report"|1|11|12];>
4:     S3:<Frame[3];Frame[7];>
5:     S4:<Frame[4];Frame[8];>
6:     SCO:<Frame[9];>;
7:     SEV:<Frame[10];>;
8:  >;
``` 

> While you can [hide](HideStatement.md) and [reveal](RevealStatement.md) statements of a Cross Examination, you can't set an initial state. Initially, all statements are revealed by default.
> This is because this feature was forgotten when Cross Examinations were implemented, and I'm too lazy to adjust the script parser for this. Oh well.

---
[Back to overview](index.md)