[Back to overview](index.md)

---
# ButtonChoice
---
- ButtonChoice (BC)
- Description: Displays up to four buttons on the bottom screen and waits until the player has clicked one.
- Parameters:
  - **Choice(s)**:  
    You can pass up to 4 choices as strings which will determine the text on the buttons. If you want less than four choices, you can use the null character (-) to leave out a choice.
  - **Frame ID(s)**:  
    For each choice, you also have to pass an ID of a frame. That frame will be executed when the player clicks on that option.

- Examples:
```
1:  ButtonChoice:["Choice 1"|"Choice 2"|"Choice 3"|"Choice 4"|1|2|3|4];
2:  BC:["Choice 1"|"Choice 2"|-|-|1|2];
3:  BC:["Choice 1"|"Choice 2"|-|"Choice 4"|1|2|-|4];
```
- Remarks:
> None

---
[Back to overview](index.md)