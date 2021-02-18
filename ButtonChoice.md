1. ButtonChoice (BC)
2. Description: Displays up to four buttons on the bottom screen for the player to choose one.
3. Parameters:

    a. Choice(s)
    
    You can pass up to 4 choices as strings which will determine the text on the buttons. If you want less than four choices, you can use the null character (-) to leave out a choice.
    
    b. Frame ID(s)
    
    For each choice, you also have to pass an ID of a frame. That frame will be executed when the player clicks on that option.
4. Examples:
```json
ButtonChoice:["Choice 1"|"Choice 2"|"Choice 3"|"Choice 4"|1|2|3|4];
BC:["Choice 1"|"Choice 2"|-|-|1|2];
BC:["Choice 1"|"Choice 2"|-|"Choice 4"|1|2|-|4];
```
5. Remarks:
> None