[Back to overview](index.md)

---
# Basics
---
Before getting into the Instructions of the **Ace Attorney Casing Tool Script (AACS)**, there is some information and terminology that you ought to know.

1. AACS is very forgiving. If you make typos or pass the wrong parameters, the erroneous lines will simply be skipped and the next instruction will be read rather than crashing the game.
    
    The exact reasons for an instruction to be ignored are the following:
    1. The instruction starts with "->" which indicates that this and any subsequent lines until "<-" are comments.
    2. The instruction cannot be interpeted. Normally caused by a typo or syntax error.
    3. There are too few parameters, or they cannot be interpreted. Some instructions require parameters, too few and the instruction will be ignored, too many and the additional parameters will be ignored. Occasionally the engine may crash if it fails to interpret a parameter.

2. **Instructions** are the actual commands for the game, and are typed out in the code editor. There are four types of Instructions: **Regular Instructions**, **Container Instructions**, **Hybrid Instructions** and **Branch Instructions**.

    **Regular Instructions** are the common instructions for actual actions that are displayed on screen like changing scenes, displaying popups, presenting evidence, or showing dialogue.
 
    **Container Instructions** work a bit differently. They contain multiple Regular Instructions. Container Instructions also have an individual ID assigned to each of them. The reason for that is simple: a Container Instruction has to be explicitly called via a regular instruction. A regular instruction is executed as soon as the engine reads the line. A Container Instructions won't be executed when it is read. This allows you, for example, to prepare cross examinations or frames that are used more than once at the top of the script file. As of now, there are three Container Instructions, which will be explained later.
 
    **Hybrid Instructions** are a mix between regular and container. In a Hybrid Instruction you can pass parameters like in a Regular Instruction, but a parameter may not only be a value, but also another Regular Instruction. Currently, Hybrid Instructions only appear in investigations and Mood Matrix sequences.

    **Branch Instructions** are conditional branches (if and else) and loops (for and while).

3. Instruction parameters are mostly optional. This means that you don't have to type them at all. If all parameters of an instruction are optional, and you decide not to use any of them, you can use a dash (-) character instead. (I.e. [FadeOutScene:[-];](FadeOutScene.md)). Be aware, that you must use this syntax. You cannot leave the Instruction brackets out (i.e. [FadeOutScene;](FadeOutScene.md)). This syntax is reserved for instructions that don't have parameters to begin with, like the [Break](Break.md) Instruction. 

	Additionally, you have to enter all parameters that come before the one you want to use as well. This means, that if you want to use the third parameter of an Instruction, you have to enter the first and second parameter as well. You can, however, use the null character (-) for them, to indicate you want to use the default value.

## Syntax
---
There are 9 important syntax elements in AACS.
1. **The semicolon**  
    Semicolons are used to finish instructions. They are required at the end of almost every instruction, save for a select few. If it is absent, the engine will skip the line and not execute the instruction.
    
2. **The instruction header**  
	All instructions, except Branch Instructions follow the same syntax.
	```
INSTRUCTIONNAME:[PARAMETERS]
	``` 
	It is important to have no whitespaces between the name, colon, and parameters.

3. **The parameter brackets []**  
	The parameter brackets are used to define the space for parameters in instructions. Single parameters are split using the pipe "\|" symbol.

4. **The Instruction brackets <>**  
	The Instruction brackets are used for, and inside, Container Instructions to contain the Regular Instructions. They are also used for statements in cross examinations.

5. **The hybrid brackets {}**  
	Within these brackets are parameters which may be values or Regular Instructions. Separated with "\|", like Regular Instructions.

6. **Comments -><-**  
	Comments are used to force the engine to ignore certain segments of script, or to write notes about the script. Technically, you are not required to use this syntax for comments, as the engine will not parse any text it cannot understand as an instruction; however, this method can cause unexpected issues.
    
	For example, you may have two lines in the script editor:
	```
1: This line is a comment, but it doesn't use the comment syntax.
2: LoadScene:["Defense"|"Phoenix"|false|false];
	```
	The result of running these two lines of script is that neither of the lines are executed. The engine does not read whitespace characters like line breaks, and it is interepreted like this:
	```
1: This line is a comment, but it doesn't use the comment syntax.LoadScene:["Defense"|"Phoenix"|false|false];
	```
	This is not a valid instruction, so all of it is skipped.

	However, were it properly stylized as a comment (aka, encapsulating it in -> and <-), it'd be executed like this:
	```
1: LoadScene:["Defense"|"Phoenix"|false|false];
	```
	Comments get removed during compilation so all that's left is the valid instruction.

7. **Null character**:  
	AACS uses a dash (-) to represent the absence of a value. If this is used, the default value for a parameter will be used. This can greatly change the behaviour of some instructions.   
	An example would be passing null to the name parameter of the [DisplayText](DisplayText.md) Instruction or to specify how many buttons should be shown in a [ButtonChoice](ButtonChoice.md) Instruction.

8. **Variables**  
	Variables are written like this:
	```
1: #(VARIABLENAME) 
	```
	And you can set them for example like this:
	```
1: Set #(VARIABLENAME) = EXPRESSION
	```
	Keep in mind, that variables behave like Regular Instructions, but have their own syntax. For more information on variables and expressions read the [Variables](Variables.md) chapter.

9. **Branch Instructions**  
	Branch Instructions are declared using the following syntax:
	```
1: INSTRUCTIONNAME #(VARIABLE) = EXPRESSION
2: (
3:   ->Your AACS here<-
4: ); 
	```
	Although Else and For are deviating from this, slightly. For more information read up on the [Branch Instruction](Branch-Instructions.md) chapter.

---
[Back to overview](index.md)