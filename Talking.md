[Back to overview](index.md)

---
# Topic
---
- **Name:** Topic
- **Description:** Talking instructions are the topics you can talk about with a character. They are built like the following scheme:
```
1:  Topic:{DISPLAY TEXT|FIRST INSTRUCTION|SECOND INSTRUCTION|HIDDEN};
```
- **Parameters:**
  - **Display Text:**  
    The text that appears in the button of that topic.
  - **First Instruction:**  
    The regular instruction that is executed the first time the player chooses that topic.
  - **Second Instruction:**  
    The regular instruction that is executed every additional time the player chooses that topic.
  - **Hidden:**  
    Determines whether the topic is hidden by default.

- Examples:
```
1:  Topic:{"Your Alibi"|PlayFrame:["LarryAlibi1"]|PlayFrame:["LarryAlibi2"]|false};
```

- Remarks
> You can define as many topics per investigation sequence as you like; however, due to the limited space, only the first 5 topics that aren't hidden will be displayed.

---
[Back to overview](index.md)