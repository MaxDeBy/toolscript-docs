1. Name: Topic

2. Description: Talking instructions are the topics you can talk about with a character. They are built like the following scheme:
```json
Topic:{DISPLAY TEXT|FIRST INSTRUCTION|SECOND INSTRUCTION|HIDDEN};
```

3. Parameters

    a. Display Text
    
    The text that appears in the button of that topic.
    
    b. First Instruction
    
    The regular instruction that is executed the first time the player chooses that topic.

    c. Second Instruction

    The regular instruction that is executed every additional time the player chooses that topic.

    d. Hidden
    
    Determines whether the topic is hidden by default.


4. Examples:
>None

5. Remarks
>You can define as many topics per investigation sequence as you like; however, due to the limited space, only the first 5 topics that aren't hidden will be displayed.