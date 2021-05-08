[Back to overview](index.md)

---
# Basics
---
Before getting into the instructions of the **Ace Attorney Casing Tool Script (AACS)**, there is some information and terminology that you ought to know.

1. AACS is very forgiving. If you make typos or pass the wrong parameters, the erroneous lines will simply be skipped and the next instruction will be read rather than crashing the game.
    
    The exact reasons for an instruction to be ignored are the following:
    1. The instruction starts with "->" which indicates that this and any subsequent lines until "<-" are comments.
    2. The instruction cannot be interpeted. Normally caused by a typo or syntax error.
    3. There are too few parameters, or they cannot be interpreted. Some instructions require parameters, too few and the instruction will be ignored, too many and the additional parameters will be ignored. Occasionally the engine may crash if it fails to interpret a parameter.

2. **Instructions** are the actual commands for the game, and are typed out in the code editor. There are four types of instructions: **Regular instructions**, **Container instructions**, **Hybrid instructions** and **Branch instructions**.

    **Regular instructions** are the common instructions for actual actions that are displayed on screen like changing scenes, displaying popups, presenting evidence, or showing dialogue.
 
    **Container instructions** work a bit differently. They contain multiple regular instructions. Container instructions also have an individual ID assigned to each of them. The reason for that is simple: a container instruction has to be explicitly called via a regular instruction. A regular instruction is executed as soon as the engine reads the line. A container instruction won't be executed when it is read. This allows you, for example, to prepare cross examinations or frames that are used more than once at the top of the script file. As of now, there are three container instructions, which will be explained later.
 
    **Hybrid instructions** are a mix between regular and container. In a hybrid instruction you can pass parameters like in a regular instruction, but a parameter may not only be a value, but also another regular instruction. Currently, hybrid instructions only appear in investigations and Mood Matrix sequences.

    **Branch instructions** are conditional branches (if and else) and loops (for and while).

## Syntax
---
There are 9 important syntax elements in AACS.
1. **The semicolon**  
    Semicolons are used to finish instructions. They are required at the end of almost every instruction, save for a select few. If it is absent, the engine will skip the line and not execute the instruction.
    
2. **The instruction header**  
	All instructions, except branch instructions follow the same syntax.
	```
INSTRUCTIONNAME:[PARAMETERS]
	``` 
	It is important to have no whitespaces between the name, colon, and parameters.

3. **The parameter brackets []**  
	The parameter brackets are used to define the space for parameters in instructions. Single parameters are split using the pipe "\|" symbol.

4. **The instruction brackets <>**  
	The instruction brackets are used for, and inside, container instructions to contain the regular instructions. They are also used for statements in cross examinations.

5. **The hybrid brackets {}**  
	Within these brackets are parameters which may be values or regular instructions. Separated with "\|", like regular instructions.

6. **Comments -><-**  
	Comments are used to force the engine to ignore certain segments of script, or to write notes about the script. Technically, you are not required to use this syntax for    comments, as the engine will not parse any text it cannot understand as an instruction; however, this method can cause unexpected issues.
    
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
	AACS uses a dash (-) to represent the absence of a value. This is used when not passing a value to a Regular Instruction is intended to achieve a different effect.   
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
	Keep in mind, that variables behave like regular instructions, but have their own syntax. For more information on variables and expressions read the [Variables](Variables.md) chapter.

9. **Branch instructions**  
	Branch instructions are declared using the following syntax:
	```
1: INSTRUCTIONNAME #(VARIABLE) = EXPRESSION
2: (
3:   ->Your AACS here<-
4: ); 
	```
	Although Else and For are deviating from this, slightly. For more information read up on the [Branch Instruction](Branch-Instructions.md) chapter.

---
[Back to overview](index.md)