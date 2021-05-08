The cross examination instruction, or for short CE instruction, is obviously used for processing a cross examination. The container itself is defined similar to a frame:


```json
CrossExamination:[ID|MODE]<

INSTRUCTIONS

;
```


 

MODE refers to how the cross examination can be finished. If set to 1, the cross examination will only end if the player pressed all statements at least once.
Every other number means a contradiction has to be found. If you want to combine it, meaning you want the cross examination to end either way, set it to 1. 

That will take care of the press condition. And to end it by objecting, execute the newly added FinishCrossExam instruction in a frame that gets executed through the PickEvidence instruction mentioned below.

 
The difference here is that you can't use any instructions you want, unlike in frames.
In a cross examination, you only can use statement instructions. Statement instructions are also container instructions, hence they use the instruction brackets "<" and ">".
But they are also limited. They are even more limited than CE instructions. They only allow two plus one optional regular instruction. Any more or any less will fail to load the script.

 

A statement instruction is built like this:

```json
SNUM:<Instruction1;Instruction2;Instruction3;>
```

(Notice that it doesn't end with a semi-colon.)

 
**NUM** is the number of the statement instruction. It always starts with "1". The upper limit is 10. So you can have a maximum of 10 statements per CE.

Now instruction 1, 2, and 3 basically can be any regular instruction you want. But it only makes sense for two instructions.

 

Instruction 1 and 2 should be a Frame or FrameS instruction. Instruction 1 will be executed when the statement is being played. So it should contain a Frame instruction that plays a frame with a green text.
Instruction 2 will be executed while pressing, meaning when the player clicks on the "Press" button.
Instruction 3 is optional. But if you use it, it **has** to be a PickEvidence instruction. Add this to the statement that contains a contradiction to make it objectionable.

 

> Attention: Currently there can only be one statement marked as "contradiction". If you add the PickEvidence to multiple statements, only the first one will be considered.

 

Then there are two other statement instructions. They don't actually have anything to do with a statement, however.
These are called SCO and SEV and each of them only allows a single regular instruction, which should be a Frame or FrameS instruction.
The SCO will be executed after the last statement has been displayed. You should use  it for discussions with the council like in the games which usually gives a vague hint on where to look for.
The SEV will be executed when the player objects (pressing "Present") in a statement that doesn't have a contradiction. 

 

An example cross examination could look like this:

 

```json
CrossExamination:[0|1]<
   S1:<Frame[1];Frame[5];>   
   S2:<Frame[2];Frame[6];PickEvidence:["Autopsy report"|1|11|12];>
   S3:<Frame[3];Frame[7];>
   S4:<Frame[4];Frame[8];>
   SCO:<Frame[9];>;
   SEV:<Frame[10];>;
>;
```


 

> While you can hide and reveal statements of a cross examination, you can't set an initial state. Initially, all statements are revealed by default.
> This is because this feature was forgotten when cross examinations were implemented, and I'm too lazy to adjust the script parser for this. Oh well.

 
