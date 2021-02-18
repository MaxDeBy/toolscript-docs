Before getting into the instructions of the **Ace Attorney Casing Tool Script (AACS)**, there is some information and terminology that you ought to know.

1. AACS is very forgiving. If you make typos or pass the wrong parameters, the erroneous lines will simply be skipped and the next instruction will be read rather than crashing the game.
    
    The exact reasons for an instruction to be ignored are the following:
    1. The instruction starts with "->" which indicates that this and any subsequent lines until "<-" are comments.
    2. The instruction cannot be interpeted. Normally caused by a typo or syntax error.
    3. There are too few parameters, or they cannot be interpreted. Some instructions require parameters, too few and the instruction will be ignored, too many and the additional parameters will be ignored. Occasionally the engine may crash if it fails to interpret a parameter.

2. **Instructions** are the actual commands for the game, and are typed out in the code editor. There are three types of instructions: **Regular instructions, Container instructions, **and** Hybrid instructions.**

    **Regular instructions** are the common instructions for actual actions that are displayed on screen like changing scenes, displaying popups, presenting evidence, or showing dialogue.
 
    **Container instructions** work a bit differently. They contain multiple regular instructions. Container instructions also have an individual ID assigned to each of them. The reason for that is simple: a container instruction has to be explicitly called via a regular instruction. A regular instruction is executed as soon as the engine reads the line. A container instruction won't be executed when it is read. This allows, for example, for you to prepare cross examinations or frames that are used more than once at the top of the script file. As of now, there are three container instructions, which will be explained later.
 
    **Hybrid instructions** are a mix between regular and container. In a hybrid instruction you can pass parameters like in a regular instruction, but a parameter may not only be a value, but also another regular instruction. Currently, hybrid instructions only appear in investigations and Mood Matrix sequences.


**Syntax**

There are 5 syntax elements in AACS.
1. **The semicolon**

    Semicolons are used to finish instructions. They are required at the end of almost every instruction, save for a select few. If it is absent, the engine will skip the line and not execute the instruction.
2. **The instruction**

    All instructions follow the same syntax. 
    ```json
    INSTRUCTIONNAME:[PARAMETERS]
    ``` 
    It is important to have no whitespaces between the name, colon, and parameters.
3. **The parameter brackets []**

    The parameter brackets are used to define the space for parameters in instructions. Single parameters are split using the pipe "|" symbol.
4. **The instruction brackets <>**

    The instruction brackets are use for, and inside, container instructions to contain the regular instructions. They are also used for statements in cross examinations.

5. **The hybrid brackets {}**

    Within these brackets are parameters which may be values or regular instructions. Separated with "|", like regular instructions.
6. **Comments -><-**

    Comments are used to force the engine to ignore certain segments of script, or to write notes about the script. Technically, you are not required to use this syntax for comments, as the engine will not parse any text it cannot understand as an instruction; however, this method can cause unexpected issues.
    
    For example, you may have two lines in the script editor:
    ```json
    1: This line is a comment, but it doesn't use the comment syntax.
    2: LoadScene:["Defense"|Phoenix"|false|false];
    ```
    The result of running these two lines of script is that neither of the lines are executed. The engine does not read whitespace characters like line breaks, and it is interepreted like this:
    ```json
    1:This line is a comment, but it doesn't use the comment syntax.LoadScene:["Defense"|Phoenix"|false|false];
    ```
   This is not a valid instruction, so all of it is skipped.